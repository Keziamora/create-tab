# create-tab
creat tab
/*
 Navicat Premium Data Transfer

 Source Server         : ccc
 Source Server Type    : MySQL
 Source Server Version : 100427
 Source Host           : localhost:3306
 Source Schema         : ioh

 Target Server Type    : MySQL
 Target Server Version : 100427
 File Encoding         : 65001

 Date: 28/12/2022 15:05:54
*/

SET NAMES utf8mb4;
SET FOREIGN_KEY_CHECKS = 0;

-- ----------------------------
-- Table structure for siteid_list
-- ----------------------------
DROP TABLE IF EXISTS `siteid_list`;
CREATE TABLE `siteid_list`  (
  `siteid` varchar(20) CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci NOT NULL,
  `cluster` varchar(100) CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci NULL DEFAULT NULL,
  PRIMARY KEY (`siteid`) USING BTREE,
  INDEX `1`(`siteid`) USING BTREE
) ENGINE = MyISAM CHARACTER SET = utf8mb4 COLLATE = utf8mb4_general_ci ROW_FORMAT = Dynamic;

-- ----------------------------
-- Table structure for siteid_lncelid_list
-- ----------------------------
DROP TABLE IF EXISTS `siteid_lncelid_list`;
CREATE TABLE `siteid_lncelid_list`  (
  `siteid` varchar(20) CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci NOT NULL,
  `lncelid` int(11) NOT NULL,
  `cluster` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci NULL DEFAULT NULL,
  PRIMARY KEY (`siteid`, `lncelid`) USING BTREE,
  INDEX `1`(`siteid`, `lncelid`) USING BTREE
) ENGINE = MyISAM CHARACTER SET = utf8mb4 COLLATE = utf8mb4_general_ci ROW_FORMAT = Dynamic;

SET FOREIGN_KEY_CHECKS = 1;
