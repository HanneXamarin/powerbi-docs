---
title: 'Error: We couldn''t find any data in your Excel workbook'
description: 'Error: We couldn''t find any data in your Excel workbook'
author: mgblythe
manager: kfile
ms.reviewer: ''

ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 12/06/2017
ms.author: mblythe

LocalizationGroup: Troubleshooting
---
# Error: We couldn't find any data in your Excel workbook

>[!NOTE]
>This article applies to Excel 2007 and later.

When you import an Excel workbook into Power BI, you may see the following error:

*Error: We couldn't find any data in your Excel workbook. Your data might not be formatted properly. You'll need to edit your workbook in Excel and then import it again.*

![](media/service-admin-troubleshoot-excel-workbook-data/pbi_wecouldntfindanydata.png)

## Quick solution
1. Edit your workbook in Excel.
2. Select the range of cells that contain your data. The first row should contain your column headers (the column names).
3. Press **Ctrl + T** to create a table.
4. Save your workbook.
5. Return to Power BI and import your workbook again, or if you're working in Excel 2016 and you've saved your workbook to OneDrive for Business, in Excel, click File > Publish.

## Details
### Cause
In Excel, you can create a **table** out of a range of cells, which makes it easier to sort, filter, and format data.

When you import an Excel workbook, Power BI looks for these tables and imports them into a dataset; if it doesn't find any tables, you'll see this error message.

### Solution
1. Open your workbook in Excel. 
    >[!NOTE]
    >The pictures here are of Excel 2013. If you're using a different version, things may look a little different, but the steps are the same.
    
    ![](media/service-admin-troubleshoot-excel-workbook-data/pbi_trb_xlwksht1.png)
2. Select the range of cells that contain your data. The first row should contain your column headers (the column names):
   
    ![](media/service-admin-troubleshoot-excel-workbook-data/pbi_trb_xlwksht2.png)
3. In the ribbon on the **INSERT** tab, click **Table**. (Or, as a shortcut, press **Ctrl + T**.)
   
    ![](media/service-admin-troubleshoot-excel-workbook-data/pbi_trb_xlwksht3.png)
4. You'll see the following dialog. Make sure **My table has headers** is checked, and select **OK**:
   
    ![](media/service-admin-troubleshoot-excel-workbook-data/pbi_trb_xlcreatetbl.png)
5. Now your data is formatted as a table:
   
    ![](media/service-admin-troubleshoot-excel-workbook-data/pbi_trb_xltbl.png)
6. Save your workbook.
7. Return to Power BI. Select Get Data at the bottom of the left navigation pane.
   
    ![](media/service-admin-troubleshoot-excel-workbook-data/pbi_getdata.png)
8. In the **Files** box, select **Get**.
   
    ![](media/service-admin-troubleshoot-excel-workbook-data/pbi_getfiles.png)
9. Import your Excel workbook again. This time, the import should find the table and succeed.
   
    If the import still fails, let us know by clicking **Community **in the help menu:
   
    ![](media/service-admin-troubleshoot-excel-workbook-data/pbi_questionmenucommunity.png)
