---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 7b3fde5feb5dae1ca064b8f5e31bbdfe03e12c7a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914805"
---
# <span data-ttu-id="0e884-101">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0e884-101">Remove-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="0e884-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0e884-102">SYNOPSIS</span></span>
<span data-ttu-id="0e884-103">Удаление шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="0e884-103">Deletes a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e884-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0e884-104">SYNTAX</span></span>

```
Remove-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e884-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e884-105">DESCRIPTION</span></span>
<span data-ttu-id="0e884-106">Шлюз локальной сети — это объект, представляющий локальное устройство VPN.</span><span class="sxs-lookup"><span data-stu-id="0e884-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="0e884-107">Командлет **Remove-AzureRmLocalNetworkGateway** удаляет объект, представляющий локальный шлюз, на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0e884-107">The **Remove-AzureRmLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="0e884-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0e884-108">EXAMPLES</span></span>

### <span data-ttu-id="0e884-109">1: Удаление шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="0e884-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="0e884-110">Удаляет объект шлюза локальной сети с именем "myLocalGW" в группе ресурсов "myRG"</span><span class="sxs-lookup"><span data-stu-id="0e884-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

<span data-ttu-id="0e884-111">Примечание. необходимо сначала удалить все подключения к шлюзу локальной сети с помощью командлета **Remove-AzureRmVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="0e884-111">Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="0e884-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0e884-112">PARAMETERS</span></span>

### <span data-ttu-id="0e884-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e884-113">-AsJob</span></span>
<span data-ttu-id="0e884-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0e884-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e884-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e884-115">-DefaultProfile</span></span>
<span data-ttu-id="0e884-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e884-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e884-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0e884-117">-Force</span></span>
<span data-ttu-id="0e884-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="0e884-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e884-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0e884-119">-Name</span></span>
<span data-ttu-id="0e884-120">Указывает имя шлюза локальной сети, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="0e884-120">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e884-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e884-121">-PassThru</span></span>
<span data-ttu-id="0e884-122">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="0e884-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0e884-123">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="0e884-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e884-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e884-124">-ResourceGroupName</span></span>
<span data-ttu-id="0e884-125">Указывает имя группы ресурсов, которая содержит шлюз локальной сети.</span><span class="sxs-lookup"><span data-stu-id="0e884-125">Specifies the name of the resource group that contains the local network gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e884-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e884-126">-Confirm</span></span>
<span data-ttu-id="0e884-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0e884-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e884-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e884-128">-WhatIf</span></span>
<span data-ttu-id="0e884-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0e884-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e884-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0e884-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e884-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e884-131">CommonParameters</span></span>
<span data-ttu-id="0e884-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0e884-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e884-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e884-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e884-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0e884-134">INPUTS</span></span>

## <span data-ttu-id="0e884-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e884-135">OUTPUTS</span></span>

## <span data-ttu-id="0e884-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="0e884-136">NOTES</span></span>

## <span data-ttu-id="0e884-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e884-137">RELATED LINKS</span></span>

[<span data-ttu-id="0e884-138">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0e884-138">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="0e884-139">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0e884-139">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="0e884-140">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0e884-140">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)


