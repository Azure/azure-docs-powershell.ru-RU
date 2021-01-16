---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: dfdd338fd5b49813d17e089755b419605761af3a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411940"
---
# <span data-ttu-id="38d01-101">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="38d01-101">Remove-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="38d01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38d01-102">SYNOPSIS</span></span>
<span data-ttu-id="38d01-103">Удаляет источник данных из учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="38d01-103">Removes a data source from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="38d01-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="38d01-104">SYNTAX</span></span>

### <span data-ttu-id="38d01-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="38d01-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38d01-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="38d01-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38d01-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38d01-107">DESCRIPTION</span></span>
<span data-ttu-id="38d01-108">Для удаления источника данных из учетной записи Azure Data Lake Analytics удаляется cmdlet **Remove-AzDataLakeAnalyticsDataSource.**</span><span class="sxs-lookup"><span data-stu-id="38d01-108">The **Remove-AzDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="38d01-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="38d01-109">EXAMPLES</span></span>

### <span data-ttu-id="38d01-110">Пример 1. Удаление источника данных</span><span class="sxs-lookup"><span data-stu-id="38d01-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="38d01-111">Эта команда удаляет источник данных AzureStorage01 из учетной записи ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="38d01-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="38d01-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38d01-112">PARAMETERS</span></span>

### <span data-ttu-id="38d01-113">-Account</span><span class="sxs-lookup"><span data-stu-id="38d01-113">-Account</span></span>
<span data-ttu-id="38d01-114">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="38d01-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="38d01-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="38d01-115">-Blob</span></span>
<span data-ttu-id="38d01-116">Имя учетной записи хранилища AzureBlob, которая нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="38d01-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38d01-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="38d01-117">-DataLakeStore</span></span>
<span data-ttu-id="38d01-118">Указывает имя учетной записи AzureData Lake Store, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="38d01-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveDataLakeStorageAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38d01-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d01-119">-DefaultProfile</span></span>
<span data-ttu-id="38d01-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="38d01-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38d01-121">-Force</span><span class="sxs-lookup"><span data-stu-id="38d01-121">-Force</span></span>
<span data-ttu-id="38d01-122">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="38d01-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d01-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38d01-123">-PassThru</span></span>
<span data-ttu-id="38d01-124">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="38d01-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="38d01-125">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="38d01-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d01-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38d01-126">-ResourceGroupName</span></span>
<span data-ttu-id="38d01-127">Имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="38d01-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38d01-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38d01-128">-Confirm</span></span>
<span data-ttu-id="38d01-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="38d01-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d01-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38d01-130">-WhatIf</span></span>
<span data-ttu-id="38d01-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38d01-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38d01-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="38d01-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d01-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d01-133">CommonParameters</span></span>
<span data-ttu-id="38d01-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38d01-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d01-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38d01-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d01-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38d01-136">INPUTS</span></span>

### <span data-ttu-id="38d01-137">System.String</span><span class="sxs-lookup"><span data-stu-id="38d01-137">System.String</span></span>

## <span data-ttu-id="38d01-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="38d01-138">OUTPUTS</span></span>

### <span data-ttu-id="38d01-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="38d01-139">System.Boolean</span></span>

## <span data-ttu-id="38d01-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="38d01-140">NOTES</span></span>

## <span data-ttu-id="38d01-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38d01-141">RELATED LINKS</span></span>

[<span data-ttu-id="38d01-142">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="38d01-142">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="38d01-143">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="38d01-143">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


