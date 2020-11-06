---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 509c80f77d48cebd101703727cefb37399ed2577
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563091"
---
# <span data-ttu-id="d2ed1-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="d2ed1-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="d2ed1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2ed1-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ed1-103">Изменяет указанного доверенного поставщика удостоверений в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d2ed1-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2ed1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2ed1-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2ed1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2ed1-105">DESCRIPTION</span></span>
<span data-ttu-id="d2ed1-106">Командлет **Set-AzureRmDataLakeStoreTrustedIdProvider** изменяет указанный доверенный поставщик удостоверений в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d2ed1-106">The **Set-AzureRmDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="d2ed1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2ed1-107">EXAMPLES</span></span>

### <span data-ttu-id="d2ed1-108">Пример 1: обновление доверенной конечной точки поставщика удостоверений</span><span class="sxs-lookup"><span data-stu-id="d2ed1-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="d2ed1-109">Это обновление поставщика endpoing для правила межсетевого экрана "MyProvider" в учетной записи "ContosoADL" на " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="d2ed1-109">This updates the provider endpoing for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="d2ed1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2ed1-110">PARAMETERS</span></span>

### <span data-ttu-id="d2ed1-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="d2ed1-111">-Account</span></span>
<span data-ttu-id="d2ed1-112">Учетная запись Data Lake Store для добавления доверенного поставщика удостоверений</span><span class="sxs-lookup"><span data-stu-id="d2ed1-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="d2ed1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ed1-113">-DefaultProfile</span></span>
<span data-ttu-id="d2ed1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d2ed1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2ed1-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d2ed1-115">-Name</span></span>
<span data-ttu-id="d2ed1-116">Имя надежного поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="d2ed1-116">The name of the trusted identity provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2ed1-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2ed1-117">-ProviderEndpoint</span></span>
<span data-ttu-id="d2ed1-118">Правильная конечная точка доверенного поставщика в формате: https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="d2ed1-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2ed1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2ed1-119">-ResourceGroupName</span></span>
<span data-ttu-id="d2ed1-120">Указывает имя группы ресурсов, которая содержит учетную запись, для которой нужно обновить доверенный поставщик удостоверений.</span><span class="sxs-lookup"><span data-stu-id="d2ed1-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2ed1-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2ed1-121">-Confirm</span></span>
<span data-ttu-id="d2ed1-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d2ed1-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ed1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2ed1-123">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ed1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ed1-124">CommonParameters</span></span>
<span data-ttu-id="d2ed1-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2ed1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ed1-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2ed1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ed1-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2ed1-127">INPUTS</span></span>

### <span data-ttu-id="d2ed1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d2ed1-128">System.String</span></span>

## <span data-ttu-id="d2ed1-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2ed1-129">OUTPUTS</span></span>

### <span data-ttu-id="d2ed1-130">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="d2ed1-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="d2ed1-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2ed1-131">NOTES</span></span>

## <span data-ttu-id="d2ed1-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2ed1-132">RELATED LINKS</span></span>
