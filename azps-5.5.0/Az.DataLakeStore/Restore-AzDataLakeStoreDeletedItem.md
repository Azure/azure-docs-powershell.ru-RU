---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 9dcc45f8f082ce59a6082ad71c2084c5df10064c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228705"
---
# <span data-ttu-id="70b95-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="70b95-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="70b95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70b95-102">SYNOPSIS</span></span>
<span data-ttu-id="70b95-103">Восстановление удаленного файла или папки в Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="70b95-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="70b95-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="70b95-104">SYNTAX</span></span>

### <span data-ttu-id="70b95-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="70b95-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="70b95-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="70b95-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70b95-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="70b95-107">DESCRIPTION</span></span>
<span data-ttu-id="70b95-108">Чтобы восстановить удаленный файл или папку в хранилище Data Lake Store, можно восстановить с его набережной файл или папку из магазина **AzDataLakeStoreDeletedItem.**</span><span class="sxs-lookup"><span data-stu-id="70b95-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="70b95-109">Требуется путь к удаленному элементу в корзине, возвращенный get-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="70b95-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>
<span data-ttu-id="70b95-110">Внимание! Неудачание файлов — это лучший способ работы.</span><span class="sxs-lookup"><span data-stu-id="70b95-110">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="70b95-111">После удаления файла его можно восстановить без каких-либо гарантий.</span><span class="sxs-lookup"><span data-stu-id="70b95-111">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="70b95-112">Использование этого API включено с помощью списка в списках.</span><span class="sxs-lookup"><span data-stu-id="70b95-112">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="70b95-113">Если ваша учетная запись ADL не находится в списке, использование этого api позволит не реализовать исключение.</span><span class="sxs-lookup"><span data-stu-id="70b95-113">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="70b95-114">Для получения дополнительных сведений и помощи обратитесь в службу поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="70b95-114">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="70b95-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="70b95-115">EXAMPLES</span></span>

### <span data-ttu-id="70b95-116">Пример 1. Восстановление файла из магазина Data Lake Store с помощью параметра -force</span><span class="sxs-lookup"><span data-stu-id="70b95-116">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
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

## <span data-ttu-id="70b95-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70b95-117">PARAMETERS</span></span>

### <span data-ttu-id="70b95-118">-Account</span><span class="sxs-lookup"><span data-stu-id="70b95-118">-Account</span></span>
<span data-ttu-id="70b95-119">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="70b95-119">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="70b95-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70b95-120">-DefaultProfile</span></span>
<span data-ttu-id="70b95-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="70b95-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70b95-122">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="70b95-122">-DeletedItem</span></span>
<span data-ttu-id="70b95-123">Удаленный объект.</span><span class="sxs-lookup"><span data-stu-id="70b95-123">The deleted item object.</span></span>

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

### <span data-ttu-id="70b95-124">-Destination</span><span class="sxs-lookup"><span data-stu-id="70b95-124">-Destination</span></span>
<span data-ttu-id="70b95-125">Путь к удаленному файлу или папке.</span><span class="sxs-lookup"><span data-stu-id="70b95-125">The destination path to where the deleted file or folder should be restored.</span></span> 

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

### <span data-ttu-id="70b95-126">-Force</span><span class="sxs-lookup"><span data-stu-id="70b95-126">-Force</span></span>
<span data-ttu-id="70b95-127">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="70b95-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="70b95-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70b95-128">-PassThru</span></span>
<span data-ttu-id="70b95-129">Возвращает boolean true при успехе.</span><span class="sxs-lookup"><span data-stu-id="70b95-129">Return boolean true on success.</span></span>

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

### <span data-ttu-id="70b95-130">-Path</span><span class="sxs-lookup"><span data-stu-id="70b95-130">-Path</span></span>
<span data-ttu-id="70b95-131">Путь к удаленному файлу или папке в корзине.</span><span class="sxs-lookup"><span data-stu-id="70b95-131">The path of the deleted file or folder in trash.</span></span>

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

### <span data-ttu-id="70b95-132">-RestoreAction</span><span class="sxs-lookup"><span data-stu-id="70b95-132">-RestoreAction</span></span>
<span data-ttu-id="70b95-133">Действие по конфликту имен назначения — "копировать" или "переописать"</span><span class="sxs-lookup"><span data-stu-id="70b95-133">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

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

### <span data-ttu-id="70b95-134">-Type</span><span class="sxs-lookup"><span data-stu-id="70b95-134">-Type</span></span>
<span data-ttu-id="70b95-135">Тип восстанавливаемой записи: "файл" или "папка"</span><span class="sxs-lookup"><span data-stu-id="70b95-135">The type of entry being restored - "file" or "folder"</span></span>

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

### <span data-ttu-id="70b95-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70b95-136">CommonParameters</span></span>
<span data-ttu-id="70b95-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70b95-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70b95-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70b95-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70b95-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70b95-139">INPUTS</span></span>

### <span data-ttu-id="70b95-140">System.String</span><span class="sxs-lookup"><span data-stu-id="70b95-140">System.String</span></span>

## <span data-ttu-id="70b95-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="70b95-141">OUTPUTS</span></span>

### <span data-ttu-id="70b95-142">Нет</span><span class="sxs-lookup"><span data-stu-id="70b95-142">None</span></span>

## <span data-ttu-id="70b95-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="70b95-143">NOTES</span></span>

## <span data-ttu-id="70b95-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="70b95-144">RELATED LINKS</span></span>

[<span data-ttu-id="70b95-145">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="70b95-145">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)