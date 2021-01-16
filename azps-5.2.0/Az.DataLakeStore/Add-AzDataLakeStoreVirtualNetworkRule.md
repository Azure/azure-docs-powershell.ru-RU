---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 8fbb586e1829cd40302ab290c2d671c67666b7e3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397476"
---
# <span data-ttu-id="6226b-101">Add-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6226b-101">Add-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="6226b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6226b-102">SYNOPSIS</span></span>
<span data-ttu-id="6226b-103">Добавляет виртуальное правило сети в указанную учетную запись Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6226b-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="6226b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6226b-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6226b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6226b-105">DESCRIPTION</span></span>
<span data-ttu-id="6226b-106">Командлет **Add-AzDataLakeStoreVirtualNetworkRule** добавляет виртуальное правило сети к указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6226b-106">The **Add-AzDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="6226b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6226b-107">EXAMPLES</span></span>

### <span data-ttu-id="6226b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6226b-108">Example 1</span></span>
```powershell
PS C:\> Add-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="6226b-109">При этом создается новое правило виртуальной сети под названием "myVNET" в учетной записи "dls" с ид подсети testId.</span><span class="sxs-lookup"><span data-stu-id="6226b-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="6226b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6226b-110">PARAMETERS</span></span>

### <span data-ttu-id="6226b-111">-Account</span><span class="sxs-lookup"><span data-stu-id="6226b-111">-Account</span></span>
<span data-ttu-id="6226b-112">Учетная запись Магазина данных для добавления виртуального правила сети в</span><span class="sxs-lookup"><span data-stu-id="6226b-112">The Data Lake Store account to add the virtual network rule to</span></span>

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

### <span data-ttu-id="6226b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6226b-113">-DefaultProfile</span></span>
<span data-ttu-id="6226b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6226b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6226b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6226b-115">-Name</span></span>
<span data-ttu-id="6226b-116">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6226b-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="6226b-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="6226b-117">-SubnetId</span></span>
<span data-ttu-id="6226b-118">SubnetId виртуального правила сети</span><span class="sxs-lookup"><span data-stu-id="6226b-118">The subnetId of the virtual network rule</span></span>

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

### <span data-ttu-id="6226b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6226b-119">-Confirm</span></span>
<span data-ttu-id="6226b-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6226b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6226b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6226b-121">-WhatIf</span></span>
<span data-ttu-id="6226b-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6226b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6226b-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6226b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6226b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6226b-124">CommonParameters</span></span>
<span data-ttu-id="6226b-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6226b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6226b-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6226b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6226b-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6226b-127">INPUTS</span></span>

### <span data-ttu-id="6226b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6226b-128">System.String</span></span>

## <span data-ttu-id="6226b-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6226b-129">OUTPUTS</span></span>

### <span data-ttu-id="6226b-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6226b-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="6226b-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6226b-131">NOTES</span></span>

## <span data-ttu-id="6226b-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6226b-132">RELATED LINKS</span></span>
