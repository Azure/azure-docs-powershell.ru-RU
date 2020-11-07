---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: 61cae1140ef0c46eee5857c15d0b6032a65caeb0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730147"
---
# <span data-ttu-id="3defb-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3defb-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="3defb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3defb-102">SYNOPSIS</span></span>
<span data-ttu-id="3defb-103">Удаление сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3defb-103">Removes a network interface.</span></span>

## <span data-ttu-id="3defb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3defb-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3defb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3defb-105">DESCRIPTION</span></span>
<span data-ttu-id="3defb-106">Командлет **Remove-AzNetworkInterface** удаляет сетевой интерфейс Azure.</span><span class="sxs-lookup"><span data-stu-id="3defb-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="3defb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3defb-107">EXAMPLES</span></span>

### <span data-ttu-id="3defb-108">Пример 1: Удаление сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="3defb-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="3defb-109">Эта команда удаляет сетевую интерфейс NetworkInterface1 в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="3defb-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="3defb-110">Так как параметр *Force* не используется, пользователю будет предложено подтвердить это действие.</span><span class="sxs-lookup"><span data-stu-id="3defb-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="3defb-111">Пример 2: Удаление сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="3defb-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="3defb-112">Эта команда удаляет все сетевые интерфейсы в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="3defb-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="3defb-113">Поскольку используется параметр *Force* , пользователь не получает запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="3defb-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="3defb-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3defb-114">PARAMETERS</span></span>

### <span data-ttu-id="3defb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3defb-115">-AsJob</span></span>
<span data-ttu-id="3defb-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3defb-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3defb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3defb-117">-DefaultProfile</span></span>
<span data-ttu-id="3defb-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3defb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3defb-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3defb-119">-Force</span></span>
<span data-ttu-id="3defb-120">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="3defb-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3defb-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3defb-121">-Name</span></span>
<span data-ttu-id="3defb-122">Указывает имя сетевого интерфейса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="3defb-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3defb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3defb-123">-PassThru</span></span>
<span data-ttu-id="3defb-124">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="3defb-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3defb-125">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3defb-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3defb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3defb-126">-ResourceGroupName</span></span>
<span data-ttu-id="3defb-127">Указывает имя группы ресурсов, которая содержит сетевой интерфейс, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="3defb-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3defb-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3defb-128">-Confirm</span></span>
<span data-ttu-id="3defb-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3defb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3defb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3defb-130">-WhatIf</span></span>
<span data-ttu-id="3defb-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3defb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3defb-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3defb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3defb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3defb-133">CommonParameters</span></span>
<span data-ttu-id="3defb-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3defb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3defb-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3defb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3defb-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3defb-136">INPUTS</span></span>

### <span data-ttu-id="3defb-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3defb-137">System.String</span></span>

## <span data-ttu-id="3defb-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3defb-138">OUTPUTS</span></span>

### <span data-ttu-id="3defb-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3defb-139">System.Boolean</span></span>

## <span data-ttu-id="3defb-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="3defb-140">NOTES</span></span>

## <span data-ttu-id="3defb-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3defb-141">RELATED LINKS</span></span>

[<span data-ttu-id="3defb-142">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3defb-142">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="3defb-143">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3defb-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="3defb-144">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3defb-144">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


