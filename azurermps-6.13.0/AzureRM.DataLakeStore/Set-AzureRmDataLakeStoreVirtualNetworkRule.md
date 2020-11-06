---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: b05158ae21219760c9c88fe9c0ae3e4978b76f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563083"
---
# <span data-ttu-id="dc5bf-101">Set-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="dc5bf-101">Set-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="dc5bf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc5bf-102">SYNOPSIS</span></span>
<span data-ttu-id="dc5bf-103">Изменяет указанное правило виртуальной сети в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="dc5bf-103">Modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc5bf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc5bf-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc5bf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc5bf-105">DESCRIPTION</span></span>
<span data-ttu-id="dc5bf-106">Командлет **Set-AzureRmDataLakeStoreVirtualNetworkRule** изменяет указанное правило виртуальной сети в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="dc5bf-106">The **Set-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="dc5bf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc5bf-107">EXAMPLES</span></span>

### <span data-ttu-id="dc5bf-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dc5bf-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "updatedId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/updatedId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="dc5bf-109">Обновление идентификатора подсети правила виртуальной сети "myVNET" в учетной записи "списки рассылки" на "updatedId"</span><span class="sxs-lookup"><span data-stu-id="dc5bf-109">Updates the subnet id of virtual network rule "myVNET" in account "dls" to "updatedId"</span></span>

## <span data-ttu-id="dc5bf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc5bf-110">PARAMETERS</span></span>

### <span data-ttu-id="dc5bf-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="dc5bf-111">-Account</span></span>
<span data-ttu-id="dc5bf-112">Учетная запись Data Lake Store для обновления правила виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="dc5bf-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="dc5bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc5bf-113">-DefaultProfile</span></span>
<span data-ttu-id="dc5bf-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc5bf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc5bf-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dc5bf-115">-Name</span></span>
<span data-ttu-id="dc5bf-116">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="dc5bf-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="dc5bf-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="dc5bf-117">-SubnetId</span></span>
<span data-ttu-id="dc5bf-118">Начало диапазона допустимых IP-адресов для правила виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="dc5bf-118">The start of the valid ip range for the virtual network rule</span></span>

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

### <span data-ttu-id="dc5bf-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc5bf-119">-Confirm</span></span>
<span data-ttu-id="dc5bf-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dc5bf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc5bf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc5bf-121">-WhatIf</span></span>
<span data-ttu-id="dc5bf-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dc5bf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc5bf-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dc5bf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc5bf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc5bf-124">CommonParameters</span></span>
<span data-ttu-id="dc5bf-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc5bf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc5bf-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc5bf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc5bf-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc5bf-127">INPUTS</span></span>

### <span data-ttu-id="dc5bf-128">System. String</span><span class="sxs-lookup"><span data-stu-id="dc5bf-128">System.String</span></span>

## <span data-ttu-id="dc5bf-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc5bf-129">OUTPUTS</span></span>

### <span data-ttu-id="dc5bf-130">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="dc5bf-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="dc5bf-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc5bf-131">NOTES</span></span>

## <span data-ttu-id="dc5bf-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc5bf-132">RELATED LINKS</span></span>
