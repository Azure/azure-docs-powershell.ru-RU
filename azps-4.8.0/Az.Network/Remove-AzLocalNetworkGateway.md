---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: 8c3741f7e1a3e25dfbc3a3b6f7fb655e5db19fe8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234936"
---
# <span data-ttu-id="5883c-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5883c-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="5883c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5883c-102">SYNOPSIS</span></span>
<span data-ttu-id="5883c-103">Удаление шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="5883c-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="5883c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5883c-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5883c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5883c-105">DESCRIPTION</span></span>
<span data-ttu-id="5883c-106">Шлюз локальной сети — это объект, представляющий локальное устройство VPN.</span><span class="sxs-lookup"><span data-stu-id="5883c-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="5883c-107">Командлет **Remove-AzLocalNetworkGateway** удаляет объект, представляющий локальный шлюз, на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5883c-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="5883c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5883c-108">EXAMPLES</span></span>

### <span data-ttu-id="5883c-109">Пример 1: Удаление шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="5883c-109">Example 1: Delete a Local Network Gateway</span></span>
```powershell
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="5883c-110">Удаляет объект шлюза локальной сети с именем "myLocalGW" в группе ресурсов "myRG" Примечание. сначала необходимо удалить все подключения к шлюзу локальной сети с помощью командлета **Remove-AzVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="5883c-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="5883c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5883c-111">PARAMETERS</span></span>

### <span data-ttu-id="5883c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5883c-112">-AsJob</span></span>
<span data-ttu-id="5883c-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5883c-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5883c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5883c-114">-DefaultProfile</span></span>
<span data-ttu-id="5883c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5883c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5883c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5883c-116">-Force</span></span>
<span data-ttu-id="5883c-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="5883c-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5883c-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5883c-118">-Name</span></span>
<span data-ttu-id="5883c-119">Указывает имя шлюза локальной сети, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5883c-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5883c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5883c-120">-PassThru</span></span>
<span data-ttu-id="5883c-121">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="5883c-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5883c-122">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5883c-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5883c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5883c-123">-ResourceGroupName</span></span>
<span data-ttu-id="5883c-124">Указывает имя группы ресурсов, которая содержит шлюз локальной сети.</span><span class="sxs-lookup"><span data-stu-id="5883c-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5883c-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5883c-125">-Confirm</span></span>
<span data-ttu-id="5883c-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5883c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5883c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5883c-127">-WhatIf</span></span>
<span data-ttu-id="5883c-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5883c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5883c-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5883c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5883c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5883c-130">CommonParameters</span></span>
<span data-ttu-id="5883c-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5883c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5883c-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5883c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5883c-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5883c-133">INPUTS</span></span>

### <span data-ttu-id="5883c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5883c-134">System.String</span></span>

## <span data-ttu-id="5883c-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5883c-135">OUTPUTS</span></span>

### <span data-ttu-id="5883c-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5883c-136">System.Boolean</span></span>

## <span data-ttu-id="5883c-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="5883c-137">NOTES</span></span>

## <span data-ttu-id="5883c-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5883c-138">RELATED LINKS</span></span>

[<span data-ttu-id="5883c-139">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5883c-139">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="5883c-140">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5883c-140">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="5883c-141">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5883c-141">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
