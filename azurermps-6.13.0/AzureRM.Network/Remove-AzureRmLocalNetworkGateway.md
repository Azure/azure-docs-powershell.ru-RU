---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: c09e812762867dc6aa89945f50d9658bb61bf5a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560044"
---
# <span data-ttu-id="188f8-101">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="188f8-101">Remove-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="188f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="188f8-102">SYNOPSIS</span></span>
<span data-ttu-id="188f8-103">Удаление шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="188f8-103">Deletes a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="188f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="188f8-104">SYNTAX</span></span>

```
Remove-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="188f8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="188f8-105">DESCRIPTION</span></span>
<span data-ttu-id="188f8-106">Шлюз локальной сети — это объект, представляющий локальное устройство VPN.</span><span class="sxs-lookup"><span data-stu-id="188f8-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="188f8-107">Командлет **Remove-AzureRmLocalNetworkGateway** удаляет объект, представляющий локальный шлюз, на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="188f8-107">The **Remove-AzureRmLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="188f8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="188f8-108">EXAMPLES</span></span>

### <span data-ttu-id="188f8-109">1: Удаление шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="188f8-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="188f8-110">Удаляет объект шлюза локальной сети с именем "myLocalGW" в группе ресурсов "myRG" Примечание. сначала необходимо удалить все подключения к шлюзу локальной сети с помощью командлета **Remove-AzureRmVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="188f8-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="188f8-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="188f8-111">PARAMETERS</span></span>

### <span data-ttu-id="188f8-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="188f8-112">-AsJob</span></span>
<span data-ttu-id="188f8-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="188f8-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="188f8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="188f8-114">-DefaultProfile</span></span>
<span data-ttu-id="188f8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="188f8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="188f8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="188f8-116">-Force</span></span>
<span data-ttu-id="188f8-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="188f8-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="188f8-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="188f8-118">-Name</span></span>
<span data-ttu-id="188f8-119">Указывает имя шлюза локальной сети, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="188f8-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="188f8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="188f8-120">-PassThru</span></span>
<span data-ttu-id="188f8-121">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="188f8-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="188f8-122">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="188f8-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="188f8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="188f8-123">-ResourceGroupName</span></span>
<span data-ttu-id="188f8-124">Указывает имя группы ресурсов, которая содержит шлюз локальной сети.</span><span class="sxs-lookup"><span data-stu-id="188f8-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="188f8-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="188f8-125">-Confirm</span></span>
<span data-ttu-id="188f8-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="188f8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="188f8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="188f8-127">-WhatIf</span></span>
<span data-ttu-id="188f8-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="188f8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="188f8-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="188f8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="188f8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="188f8-130">CommonParameters</span></span>
<span data-ttu-id="188f8-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="188f8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="188f8-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="188f8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="188f8-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="188f8-133">INPUTS</span></span>

### <span data-ttu-id="188f8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="188f8-134">System.String</span></span>

## <span data-ttu-id="188f8-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="188f8-135">OUTPUTS</span></span>

### <span data-ttu-id="188f8-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="188f8-136">System.Boolean</span></span>

## <span data-ttu-id="188f8-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="188f8-137">NOTES</span></span>

## <span data-ttu-id="188f8-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="188f8-138">RELATED LINKS</span></span>

[<span data-ttu-id="188f8-139">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="188f8-139">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="188f8-140">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="188f8-140">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="188f8-141">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="188f8-141">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)


