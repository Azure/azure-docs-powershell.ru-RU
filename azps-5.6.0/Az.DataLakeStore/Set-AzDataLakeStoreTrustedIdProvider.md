---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 7efe0e21b6b433160eab36856d3419dc918cbfc4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995588"
---
# <span data-ttu-id="64bb2-101">Set-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="64bb2-101">Set-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="64bb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="64bb2-103">Изменяет указанного надежного поставщика удостоверений в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="64bb2-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="64bb2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="64bb2-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64bb2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64bb2-105">DESCRIPTION</span></span>
<span data-ttu-id="64bb2-106">**Cmdlet Set-AzDataLakeStoreTrustedIdProvider** изменяет указанного надежного поставщика удостоверений в указанном магазине Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="64bb2-106">The **Set-AzDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="64bb2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="64bb2-107">EXAMPLES</span></span>

### <span data-ttu-id="64bb2-108">Пример 1. Обновление конечной точки надежного поставщика удостоверений</span><span class="sxs-lookup"><span data-stu-id="64bb2-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="64bb2-109">Это обновление конечной точки поставщика для правила брандмауэра "MyProvider" в учетной записи "ContosoADL" на https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="64bb2-109">This updates the provider endpoint for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="64bb2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64bb2-110">PARAMETERS</span></span>

### <span data-ttu-id="64bb2-111">-Account</span><span class="sxs-lookup"><span data-stu-id="64bb2-111">-Account</span></span>
<span data-ttu-id="64bb2-112">Учетная запись Магазина данных для добавления надежного поставщика удостоверений в</span><span class="sxs-lookup"><span data-stu-id="64bb2-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="64bb2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64bb2-113">-DefaultProfile</span></span>
<span data-ttu-id="64bb2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="64bb2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64bb2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="64bb2-115">-Name</span></span>
<span data-ttu-id="64bb2-116">Имя надежного поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="64bb2-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="64bb2-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="64bb2-117">-ProviderEndpoint</span></span>
<span data-ttu-id="64bb2-118">Действительная конечная точка надежного поставщика в формате: https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="64bb2-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="64bb2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64bb2-119">-ResourceGroupName</span></span>
<span data-ttu-id="64bb2-120">Имя группы ресурсов, которая содержит учетную запись для обновления надежного поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="64bb2-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="64bb2-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64bb2-121">-Confirm</span></span>
<span data-ttu-id="64bb2-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64bb2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64bb2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64bb2-123">-WhatIf</span></span>
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

### <span data-ttu-id="64bb2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64bb2-124">CommonParameters</span></span>
<span data-ttu-id="64bb2-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64bb2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64bb2-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64bb2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64bb2-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64bb2-127">INPUTS</span></span>

### <span data-ttu-id="64bb2-128">System.String</span><span class="sxs-lookup"><span data-stu-id="64bb2-128">System.String</span></span>

## <span data-ttu-id="64bb2-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="64bb2-129">OUTPUTS</span></span>

### <span data-ttu-id="64bb2-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="64bb2-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="64bb2-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="64bb2-131">NOTES</span></span>

## <span data-ttu-id="64bb2-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64bb2-132">RELATED LINKS</span></span>
