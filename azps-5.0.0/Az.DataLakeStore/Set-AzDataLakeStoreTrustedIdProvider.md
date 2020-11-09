---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c4de7a926e4095ad8bb45a25647305617988330d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313223"
---
# <span data-ttu-id="a7d96-101">Set-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="a7d96-101">Set-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="a7d96-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7d96-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d96-103">Изменяет указанного доверенного поставщика удостоверений в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a7d96-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="a7d96-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7d96-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7d96-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7d96-105">DESCRIPTION</span></span>
<span data-ttu-id="a7d96-106">Командлет **Set-AzDataLakeStoreTrustedIdProvider** изменяет указанный доверенный поставщик удостоверений в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a7d96-106">The **Set-AzDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="a7d96-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7d96-107">EXAMPLES</span></span>

### <span data-ttu-id="a7d96-108">Пример 1: обновление доверенной конечной точки поставщика удостоверений</span><span class="sxs-lookup"><span data-stu-id="a7d96-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="a7d96-109">Это действие обновит конечную точку поставщика для правила брандмауэра "MyProvider" в учетной записи "ContosoADL" в " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="a7d96-109">This updates the provider endpoint for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="a7d96-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7d96-110">PARAMETERS</span></span>

### <span data-ttu-id="a7d96-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="a7d96-111">-Account</span></span>
<span data-ttu-id="a7d96-112">Учетная запись Data Lake Store для добавления доверенного поставщика удостоверений</span><span class="sxs-lookup"><span data-stu-id="a7d96-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="a7d96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d96-113">-DefaultProfile</span></span>
<span data-ttu-id="a7d96-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a7d96-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7d96-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a7d96-115">-Name</span></span>
<span data-ttu-id="a7d96-116">Имя надежного поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="a7d96-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="a7d96-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7d96-117">-ProviderEndpoint</span></span>
<span data-ttu-id="a7d96-118">Правильная конечная точка доверенного поставщика в формате: https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="a7d96-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="a7d96-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7d96-119">-ResourceGroupName</span></span>
<span data-ttu-id="a7d96-120">Указывает имя группы ресурсов, которая содержит учетную запись, для которой нужно обновить доверенный поставщик удостоверений.</span><span class="sxs-lookup"><span data-stu-id="a7d96-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="a7d96-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7d96-121">-Confirm</span></span>
<span data-ttu-id="a7d96-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a7d96-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7d96-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7d96-123">-WhatIf</span></span>
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

### <span data-ttu-id="a7d96-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d96-124">CommonParameters</span></span>
<span data-ttu-id="a7d96-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7d96-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d96-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7d96-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d96-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7d96-127">INPUTS</span></span>

### <span data-ttu-id="a7d96-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a7d96-128">System.String</span></span>

## <span data-ttu-id="a7d96-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7d96-129">OUTPUTS</span></span>

### <span data-ttu-id="a7d96-130">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="a7d96-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="a7d96-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7d96-131">NOTES</span></span>

## <span data-ttu-id="a7d96-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7d96-132">RELATED LINKS</span></span>
