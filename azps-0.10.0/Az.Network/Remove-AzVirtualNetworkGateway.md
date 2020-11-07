---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: bb63f9d56dc78943f9232107e39188ae3d29f43f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911109"
---
# <span data-ttu-id="a1068-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a1068-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="a1068-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1068-102">SYNOPSIS</span></span>
<span data-ttu-id="a1068-103">Удаление шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="a1068-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="a1068-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1068-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1068-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1068-105">DESCRIPTION</span></span>
<span data-ttu-id="a1068-106">Шлюз виртуальной сети — это объект, представляющий ваш шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="a1068-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="a1068-107">Командлет **Get-AzVirtualNetworkGateway** возвращает объект шлюза в Azure на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1068-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="a1068-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1068-108">EXAMPLES</span></span>

### <span data-ttu-id="a1068-109">1: Удаление шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="a1068-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="a1068-110">Удаляет объект шлюза виртуальной сети с именем "myGateway" в группе ресурсов "myRG"</span><span class="sxs-lookup"><span data-stu-id="a1068-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

<span data-ttu-id="a1068-111">Примечание. необходимо сначала удалить все подключения к шлюзу виртуальной сети с помощью командлета **Remove-AzVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="a1068-111">Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="a1068-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1068-112">PARAMETERS</span></span>

### <span data-ttu-id="a1068-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1068-113">-AsJob</span></span>
<span data-ttu-id="a1068-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a1068-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1068-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1068-115">-DefaultProfile</span></span>
<span data-ttu-id="a1068-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1068-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1068-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a1068-117">-Force</span></span>
<span data-ttu-id="a1068-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a1068-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a1068-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a1068-119">-Name</span></span>
<span data-ttu-id="a1068-120">Указывает имя шлюза виртуальной сети, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="a1068-120">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a1068-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1068-121">-PassThru</span></span>
<span data-ttu-id="a1068-122">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="a1068-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a1068-123">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a1068-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a1068-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1068-124">-ResourceGroupName</span></span>
<span data-ttu-id="a1068-125">Указывает имя группы ресурсов, которая содержит шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a1068-125">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="a1068-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1068-126">-Confirm</span></span>
<span data-ttu-id="a1068-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a1068-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1068-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1068-128">-WhatIf</span></span>
<span data-ttu-id="a1068-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a1068-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1068-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a1068-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1068-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1068-131">CommonParameters</span></span>
<span data-ttu-id="a1068-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1068-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1068-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1068-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1068-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1068-134">INPUTS</span></span>

## <span data-ttu-id="a1068-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1068-135">OUTPUTS</span></span>

## <span data-ttu-id="a1068-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1068-136">NOTES</span></span>

## <span data-ttu-id="a1068-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1068-137">RELATED LINKS</span></span>

