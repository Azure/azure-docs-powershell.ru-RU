---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: b6647ab3b729ab76d3cc02687bcd8dc342e788b4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397484"
---
# <span data-ttu-id="9506e-101">Add-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="9506e-101">Add-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="9506e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9506e-102">SYNOPSIS</span></span>
<span data-ttu-id="9506e-103">Добавляет надежного поставщика удостоверений в указанную учетную запись Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9506e-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="9506e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9506e-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9506e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9506e-105">DESCRIPTION</span></span>
<span data-ttu-id="9506e-106">Cmdlet **Add-AzDataLakeStoreTrustedIdProvider** добавляет надежного поставщика удостоверений в указанную учетную запись Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9506e-106">The **Add-AzDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="9506e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9506e-107">EXAMPLES</span></span>

### <span data-ttu-id="9506e-108">Пример 1. Добавление надежного поставщика удостоверений</span><span class="sxs-lookup"><span data-stu-id="9506e-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="9506e-109">Добавляет поставщика "MyProvider" к учетной записи "ContosoADL" с конечной точкой поставщика https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="9506e-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="9506e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9506e-110">PARAMETERS</span></span>

### <span data-ttu-id="9506e-111">-Account</span><span class="sxs-lookup"><span data-stu-id="9506e-111">-Account</span></span>
<span data-ttu-id="9506e-112">Имя учетной записи Для добавления указанного надежного поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="9506e-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

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

### <span data-ttu-id="9506e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9506e-113">-DefaultProfile</span></span>
<span data-ttu-id="9506e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9506e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9506e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9506e-115">-Name</span></span>
<span data-ttu-id="9506e-116">Имя добавляемого поставщика доверенных удостоверений</span><span class="sxs-lookup"><span data-stu-id="9506e-116">The name of the trusted identity provider to add</span></span>

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

### <span data-ttu-id="9506e-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="9506e-117">-ProviderEndpoint</span></span>
<span data-ttu-id="9506e-118">Действительная конечная точка надежного поставщика в формате: https://sts.windows.net/ \<provider identity\> "</span><span class="sxs-lookup"><span data-stu-id="9506e-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

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

### <span data-ttu-id="9506e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9506e-119">-ResourceGroupName</span></span>
<span data-ttu-id="9506e-120">Имя группы ресурсов, для которой нужно добавить учетную запись надежного поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="9506e-120">Name of resource group under which the account to add the trusted identity provider is.</span></span>

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

### <span data-ttu-id="9506e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9506e-121">-Confirm</span></span>
<span data-ttu-id="9506e-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9506e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9506e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9506e-123">-WhatIf</span></span>
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

### <span data-ttu-id="9506e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9506e-124">CommonParameters</span></span>
<span data-ttu-id="9506e-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9506e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9506e-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9506e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9506e-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9506e-127">INPUTS</span></span>

### <span data-ttu-id="9506e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="9506e-128">System.String</span></span>

## <span data-ttu-id="9506e-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9506e-129">OUTPUTS</span></span>

### <span data-ttu-id="9506e-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="9506e-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="9506e-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9506e-131">NOTES</span></span>

## <span data-ttu-id="9506e-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9506e-132">RELATED LINKS</span></span>