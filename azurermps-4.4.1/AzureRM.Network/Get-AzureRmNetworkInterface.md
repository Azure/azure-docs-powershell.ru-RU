---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterface.md
ms.openlocfilehash: 42d5ef31b49f8abe5c8e582e0a85e8766a71b9a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568736"
---
# <span data-ttu-id="72a0a-101">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="72a0a-101">Get-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="72a0a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="72a0a-102">SYNOPSIS</span></span>
<span data-ttu-id="72a0a-103">Возвращает сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="72a0a-103">Gets a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72a0a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="72a0a-104">SYNTAX</span></span>

### <span data-ttu-id="72a0a-105">NoExpandStandAloneNic (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="72a0a-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72a0a-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="72a0a-106">ExpandStandAloneNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72a0a-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="72a0a-107">NoExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72a0a-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="72a0a-108">ExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72a0a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72a0a-109">DESCRIPTION</span></span>
<span data-ttu-id="72a0a-110">Командлет **Get-AzureRmNetworkInterface** получает сетевой интерфейс Azure или список сетевых интерфейсов Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="72a0a-110">The **Get-AzureRmNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="72a0a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="72a0a-111">EXAMPLES</span></span>

### <span data-ttu-id="72a0a-112">Пример 1: получение всех сетевых интерфейсов</span><span class="sxs-lookup"><span data-stu-id="72a0a-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzureRmNetworkInterface
```

<span data-ttu-id="72a0a-113">Эта команда получает все сетевые интерфейсы для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="72a0a-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="72a0a-114">Пример 2: получение всех сетевых интерфейсов с определенным состоянием подготовки</span><span class="sxs-lookup"><span data-stu-id="72a0a-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="72a0a-115">Эта команда получает все сетевые интерфейсы в группе ресурсов с именем ResourceGroup1, для которой успешно определено состояние подготовки.</span><span class="sxs-lookup"><span data-stu-id="72a0a-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="72a0a-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="72a0a-116">PARAMETERS</span></span>

### <span data-ttu-id="72a0a-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="72a0a-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72a0a-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="72a0a-118">-Name</span></span>
<span data-ttu-id="72a0a-119">Указывает имя сетевого интерфейса, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="72a0a-119">Specifies the name of the network interface that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic, NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72a0a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72a0a-120">-ResourceGroupName</span></span>
<span data-ttu-id="72a0a-121">Указывает имя группы ресурсов, из которой этот командлет получает сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="72a0a-121">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, NoExpandScaleSetNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72a0a-122">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="72a0a-122">-VirtualMachineIndex</span></span>
<span data-ttu-id="72a0a-123">Указывает индекс виртуальной машины в наборе масштабов виртуальных машин, на основе которого этот командлет получает сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="72a0a-123">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72a0a-124">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="72a0a-124">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="72a0a-125">Указывает имя набора масштабов виртуальной машины, на основе которого этот командлет получает сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="72a0a-125">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72a0a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72a0a-126">-DefaultProfile</span></span>
<span data-ttu-id="72a0a-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="72a0a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72a0a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72a0a-128">CommonParameters</span></span>
<span data-ttu-id="72a0a-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="72a0a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72a0a-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72a0a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72a0a-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="72a0a-131">INPUTS</span></span>

## <span data-ttu-id="72a0a-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="72a0a-132">OUTPUTS</span></span>

### <span data-ttu-id="72a0a-133">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="72a0a-133">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="72a0a-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="72a0a-134">NOTES</span></span>

## <span data-ttu-id="72a0a-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72a0a-135">RELATED LINKS</span></span>

[<span data-ttu-id="72a0a-136">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="72a0a-136">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="72a0a-137">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="72a0a-137">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="72a0a-138">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="72a0a-138">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


