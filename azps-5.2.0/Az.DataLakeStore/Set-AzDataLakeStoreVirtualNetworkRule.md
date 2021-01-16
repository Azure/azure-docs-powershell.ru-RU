---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 1c649a63e8ba57a3d2e9f9af28e0ce4b12ca9a0d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407412"
---
# <span data-ttu-id="c2beb-101">Set-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c2beb-101">Set-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="c2beb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2beb-102">SYNOPSIS</span></span>
<span data-ttu-id="c2beb-103">Изменяет указанное правило виртуальной сети в указанном Хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="c2beb-103">Modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="c2beb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c2beb-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2beb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2beb-105">DESCRIPTION</span></span>
<span data-ttu-id="c2beb-106">Командлет **Set-AzDataLakeStoreVirtualNetworkRule** изменяет указанное правило виртуальной сети в указанном хранилище для озера данных.</span><span class="sxs-lookup"><span data-stu-id="c2beb-106">The **Set-AzDataLakeStoreVirtualNetworkRule** cmdlet modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="c2beb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c2beb-107">EXAMPLES</span></span>

### <span data-ttu-id="c2beb-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c2beb-108">Example 1</span></span>
```powershell
PS C:\> Set-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "updatedId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/updatedId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="c2beb-109">Обновление id подсети виртуального правила сети "myVNET" в учетной записи "dls" на updatedId.</span><span class="sxs-lookup"><span data-stu-id="c2beb-109">Updates the subnet id of virtual network rule "myVNET" in account "dls" to "updatedId"</span></span>

## <span data-ttu-id="c2beb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2beb-110">PARAMETERS</span></span>

### <span data-ttu-id="c2beb-111">-Account</span><span class="sxs-lookup"><span data-stu-id="c2beb-111">-Account</span></span>
<span data-ttu-id="c2beb-112">Учетная запись Магазина данных для обновления виртуального правила сети в</span><span class="sxs-lookup"><span data-stu-id="c2beb-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="c2beb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2beb-113">-DefaultProfile</span></span>
<span data-ttu-id="c2beb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2beb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2beb-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c2beb-115">-Name</span></span>
<span data-ttu-id="c2beb-116">Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="c2beb-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="c2beb-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c2beb-117">-SubnetId</span></span>
<span data-ttu-id="c2beb-118">Начало допустимого диапазона IP-адресов для виртуального правила сети</span><span class="sxs-lookup"><span data-stu-id="c2beb-118">The start of the valid ip range for the virtual network rule</span></span>

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

### <span data-ttu-id="c2beb-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2beb-119">-Confirm</span></span>
<span data-ttu-id="c2beb-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2beb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2beb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2beb-121">-WhatIf</span></span>
<span data-ttu-id="c2beb-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2beb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2beb-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c2beb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2beb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2beb-124">CommonParameters</span></span>
<span data-ttu-id="c2beb-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2beb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2beb-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2beb-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2beb-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2beb-127">INPUTS</span></span>

### <span data-ttu-id="c2beb-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c2beb-128">System.String</span></span>

## <span data-ttu-id="c2beb-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c2beb-129">OUTPUTS</span></span>

### <span data-ttu-id="c2beb-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c2beb-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="c2beb-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c2beb-131">NOTES</span></span>

## <span data-ttu-id="c2beb-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2beb-132">RELATED LINKS</span></span>
