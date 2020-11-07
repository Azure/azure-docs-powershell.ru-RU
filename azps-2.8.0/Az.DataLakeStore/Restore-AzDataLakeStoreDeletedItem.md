---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 7df59f75200bbc0d52c595c263228d7bf9801486
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721279"
---
# <span data-ttu-id="2b191-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="2b191-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="2b191-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b191-102">SYNOPSIS</span></span>
<span data-ttu-id="2b191-103">Восстановление удаленного файла или папки в Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="2b191-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="2b191-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b191-104">SYNTAX</span></span>

### <span data-ttu-id="2b191-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2b191-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b191-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2b191-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b191-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b191-107">DESCRIPTION</span></span>
<span data-ttu-id="2b191-108">Командлет **RESTORE-AzDataLakeStoreDeletedItem** восстанавливает удаленный файл или папку в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2b191-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="2b191-109">Требуется путь удаленного элемента в корзине, возвращенной функцией Get-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="2b191-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>

## <span data-ttu-id="2b191-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b191-110">EXAMPLES</span></span>

### <span data-ttu-id="2b191-111">Пример 1: восстановление файла из режима Data Lake Store с помощью параметра-Force</span><span class="sxs-lookup"><span data-stu-id="2b191-111">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
```
PS > Restore-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Path 927e8fb1-a287-4353-b50e-3b4a39ae4088 -Destination adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 -Type "file" -Force
PS >

### Example 2: Restore a file from Data Lake Store using user confirmation

PS > restore-azdatalakestoredeleteditem -account ml1ptrashtest -path 927e8fb1-a287-4353-b50e-3b4a39ae4088 -destination adl://ml1ptrashtest.azuredatalake.com/test4/file_1115 -type file

Restore user data ?
From - 927e8fb1-a287-4353-b50e-3b4a39ae4088
To   - adl://ml1ptrashtest.azuredatalake.com/test4/file_1115
Type - file
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
PS >
```

## <span data-ttu-id="2b191-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b191-112">PARAMETERS</span></span>

### <span data-ttu-id="2b191-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="2b191-113">-Account</span></span>
<span data-ttu-id="2b191-114">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2b191-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b191-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b191-115">-DefaultProfile</span></span>
<span data-ttu-id="2b191-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b191-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b191-117">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="2b191-117">-DeletedItem</span></span>
<span data-ttu-id="2b191-118">Объект удаленного элемента.</span><span class="sxs-lookup"><span data-stu-id="2b191-118">The deleted item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b191-119">-Destination</span><span class="sxs-lookup"><span data-stu-id="2b191-119">-Destination</span></span>
<span data-ttu-id="2b191-120">Конечный путь к папке, в которую нужно восстановить удаленный файл или папку.</span><span class="sxs-lookup"><span data-stu-id="2b191-120">The destination path to where the deleted file or folder should be restored.</span></span> 

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b191-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2b191-121">-Force</span></span>
<span data-ttu-id="2b191-122">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="2b191-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b191-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b191-123">-PassThru</span></span>
<span data-ttu-id="2b191-124">Возвращает логическое значение истина в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="2b191-124">Return boolean true on success.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b191-125">-Path</span><span class="sxs-lookup"><span data-stu-id="2b191-125">-Path</span></span>
<span data-ttu-id="2b191-126">Путь удаленного файла или папки в корзине.</span><span class="sxs-lookup"><span data-stu-id="2b191-126">The path of the deleted file or folder in trash.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b191-127">-RestoreAction</span><span class="sxs-lookup"><span data-stu-id="2b191-127">-RestoreAction</span></span>
<span data-ttu-id="2b191-128">Действие, которое необходимо предпринять при конфликтах конечных имен: "Копировать" или "перезаписать"</span><span class="sxs-lookup"><span data-stu-id="2b191-128">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b191-129">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="2b191-129">-Type</span></span>
<span data-ttu-id="2b191-130">Тип восстанавливаемого элемента: "файл" или "папка"</span><span class="sxs-lookup"><span data-stu-id="2b191-130">The type of entry being restored - "file" or "folder"</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b191-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b191-131">CommonParameters</span></span>
<span data-ttu-id="2b191-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b191-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b191-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b191-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b191-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b191-134">INPUTS</span></span>

### <span data-ttu-id="2b191-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2b191-135">System.String</span></span>

## <span data-ttu-id="2b191-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b191-136">OUTPUTS</span></span>

### <span data-ttu-id="2b191-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="2b191-137">None</span></span>

## <span data-ttu-id="2b191-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b191-138">NOTES</span></span>

## <span data-ttu-id="2b191-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b191-139">RELATED LINKS</span></span>

[<span data-ttu-id="2b191-140">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="2b191-140">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)