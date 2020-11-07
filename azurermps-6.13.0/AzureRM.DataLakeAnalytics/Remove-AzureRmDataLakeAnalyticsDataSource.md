---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 43f9c55e6da93392e95191d1b601f771221e1caa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732966"
---
# <span data-ttu-id="1677b-101">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1677b-101">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="1677b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1677b-102">SYNOPSIS</span></span>
<span data-ttu-id="1677b-103">Удаляет источник данных из учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1677b-103">Removes a data source from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1677b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1677b-104">SYNTAX</span></span>

### <span data-ttu-id="1677b-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1677b-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1677b-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1677b-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1677b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1677b-107">DESCRIPTION</span></span>
<span data-ttu-id="1677b-108">Командлет **Remove-AzureRmDataLakeAnalyticsDataSource** удаляет источник данных из учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1677b-108">The **Remove-AzureRmDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="1677b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1677b-109">EXAMPLES</span></span>

### <span data-ttu-id="1677b-110">Пример 1: удаление источника данных</span><span class="sxs-lookup"><span data-stu-id="1677b-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="1677b-111">Эта команда удаляет источник данных с именем AzureStorage01 из учетной записи с именем ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="1677b-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="1677b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1677b-112">PARAMETERS</span></span>

### <span data-ttu-id="1677b-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="1677b-113">-Account</span></span>
<span data-ttu-id="1677b-114">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1677b-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="1677b-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="1677b-115">-Blob</span></span>
<span data-ttu-id="1677b-116">Указывает имя учетной записи хранения AzureBlob, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="1677b-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

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

### <span data-ttu-id="1677b-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1677b-117">-DataLakeStore</span></span>
<span data-ttu-id="1677b-118">Указывает имя учетной записи AzureData Lake Store, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="1677b-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

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

### <span data-ttu-id="1677b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1677b-119">-DefaultProfile</span></span>
<span data-ttu-id="1677b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1677b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1677b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1677b-121">-Force</span></span>
<span data-ttu-id="1677b-122">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="1677b-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1677b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1677b-123">-PassThru</span></span>
<span data-ttu-id="1677b-124">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="1677b-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1677b-125">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1677b-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1677b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1677b-126">-ResourceGroupName</span></span>
<span data-ttu-id="1677b-127">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1677b-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="1677b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1677b-128">-Confirm</span></span>
<span data-ttu-id="1677b-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1677b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1677b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1677b-130">-WhatIf</span></span>
<span data-ttu-id="1677b-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1677b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1677b-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1677b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1677b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1677b-133">CommonParameters</span></span>
<span data-ttu-id="1677b-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1677b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1677b-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1677b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1677b-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1677b-136">INPUTS</span></span>

### <span data-ttu-id="1677b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1677b-137">System.String</span></span>

## <span data-ttu-id="1677b-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1677b-138">OUTPUTS</span></span>

### <span data-ttu-id="1677b-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1677b-139">System.Boolean</span></span>

## <span data-ttu-id="1677b-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="1677b-140">NOTES</span></span>

## <span data-ttu-id="1677b-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1677b-141">RELATED LINKS</span></span>

[<span data-ttu-id="1677b-142">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1677b-142">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="1677b-143">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1677b-143">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


