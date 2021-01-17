---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 95e18d7e36122ed199b4a4c880b4fc918f1164f5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403100"
---
# <span data-ttu-id="98494-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="98494-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="98494-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98494-102">SYNOPSIS</span></span>
<span data-ttu-id="98494-103">Возвращает указанные правила виртуальной сети в указанном Магазине для озера Данных.</span><span class="sxs-lookup"><span data-stu-id="98494-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="98494-104">Если виртуальное правило сети не задано, будут перечислены все правила виртуальной сети для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="98494-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="98494-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="98494-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98494-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98494-106">DESCRIPTION</span></span>
<span data-ttu-id="98494-107">Этот Get-AzDataLakeStoreVirtualNetworkRule возвращает указанные правила виртуальной сети в указанном магазине.</span><span class="sxs-lookup"><span data-stu-id="98494-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="98494-108">Если правило виртуальной сети не задано, будут перечислены все правила виртуальной сети для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="98494-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="98494-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="98494-109">EXAMPLES</span></span>

### <span data-ttu-id="98494-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="98494-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="98494-111">Возвращает правило виртуальной сети с именем "myVNET" из учетной записи "dls"</span><span class="sxs-lookup"><span data-stu-id="98494-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="98494-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98494-112">PARAMETERS</span></span>

### <span data-ttu-id="98494-113">-Account</span><span class="sxs-lookup"><span data-stu-id="98494-113">-Account</span></span>
<span data-ttu-id="98494-114">Учетная запись Data Lake Store для получения виртуального правила сети в</span><span class="sxs-lookup"><span data-stu-id="98494-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="98494-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98494-115">-DefaultProfile</span></span>
<span data-ttu-id="98494-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98494-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98494-117">-Name</span><span class="sxs-lookup"><span data-stu-id="98494-117">-Name</span></span>
<span data-ttu-id="98494-118">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="98494-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="98494-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98494-119">CommonParameters</span></span>
<span data-ttu-id="98494-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98494-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98494-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98494-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98494-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98494-122">INPUTS</span></span>

### <span data-ttu-id="98494-123">System.String</span><span class="sxs-lookup"><span data-stu-id="98494-123">System.String</span></span>

## <span data-ttu-id="98494-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="98494-124">OUTPUTS</span></span>

### <span data-ttu-id="98494-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="98494-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="98494-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="98494-126">NOTES</span></span>

## <span data-ttu-id="98494-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98494-127">RELATED LINKS</span></span>
