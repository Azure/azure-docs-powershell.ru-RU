---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: 403c41de0359f2d857d2c86b772e4af419640f2a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909481"
---
# <span data-ttu-id="edd1c-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="edd1c-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="edd1c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="edd1c-102">SYNOPSIS</span></span>
<span data-ttu-id="edd1c-103">Удаление сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="edd1c-103">Removes a network interface.</span></span>

## <span data-ttu-id="edd1c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="edd1c-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edd1c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="edd1c-105">DESCRIPTION</span></span>
<span data-ttu-id="edd1c-106">Командлет **Remove-AzNetworkInterface** удаляет сетевой интерфейс Azure.</span><span class="sxs-lookup"><span data-stu-id="edd1c-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="edd1c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="edd1c-107">EXAMPLES</span></span>

### <span data-ttu-id="edd1c-108">Пример 1: Удаление сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="edd1c-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="edd1c-109">Эта команда удаляет сетевую интерфейс NetworkInterface1 в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="edd1c-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="edd1c-110">Так как параметр *Force* не используется, пользователю будет предложено подтвердить это действие.</span><span class="sxs-lookup"><span data-stu-id="edd1c-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="edd1c-111">Пример 2: Удаление сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="edd1c-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="edd1c-112">Эта команда удаляет все сетевые интерфейсы в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="edd1c-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="edd1c-113">Поскольку используется параметр *Force* , пользователь не получает запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="edd1c-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="edd1c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="edd1c-114">PARAMETERS</span></span>

### <span data-ttu-id="edd1c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="edd1c-115">-AsJob</span></span>
<span data-ttu-id="edd1c-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="edd1c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="edd1c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edd1c-117">-DefaultProfile</span></span>
<span data-ttu-id="edd1c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="edd1c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edd1c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="edd1c-119">-Force</span></span>
<span data-ttu-id="edd1c-120">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="edd1c-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="edd1c-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="edd1c-121">-Name</span></span>
<span data-ttu-id="edd1c-122">Указывает имя сетевого интерфейса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="edd1c-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="edd1c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edd1c-123">-PassThru</span></span>
<span data-ttu-id="edd1c-124">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="edd1c-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="edd1c-125">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="edd1c-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="edd1c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edd1c-126">-ResourceGroupName</span></span>
<span data-ttu-id="edd1c-127">Указывает имя группы ресурсов, которая содержит сетевой интерфейс, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="edd1c-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="edd1c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="edd1c-128">-Confirm</span></span>
<span data-ttu-id="edd1c-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="edd1c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edd1c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edd1c-130">-WhatIf</span></span>
<span data-ttu-id="edd1c-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="edd1c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edd1c-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="edd1c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edd1c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edd1c-133">CommonParameters</span></span>
<span data-ttu-id="edd1c-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="edd1c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edd1c-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edd1c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edd1c-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="edd1c-136">INPUTS</span></span>

## <span data-ttu-id="edd1c-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="edd1c-137">OUTPUTS</span></span>

## <span data-ttu-id="edd1c-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="edd1c-138">NOTES</span></span>

## <span data-ttu-id="edd1c-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="edd1c-139">RELATED LINKS</span></span>

[<span data-ttu-id="edd1c-140">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="edd1c-140">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="edd1c-141">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="edd1c-141">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="edd1c-142">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="edd1c-142">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


