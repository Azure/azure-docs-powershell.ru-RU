---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: 54bc4a3b9875f68df8a7c824c7e4f754e6f35a4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993653"
---
# <span data-ttu-id="471b6-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="471b6-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="471b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="471b6-102">SYNOPSIS</span></span>
<span data-ttu-id="471b6-103">Удаляет сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="471b6-103">Removes a network interface.</span></span>

## <span data-ttu-id="471b6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="471b6-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="471b6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="471b6-105">DESCRIPTION</span></span>
<span data-ttu-id="471b6-106">Командлет **Remove-AzNetworkInterface** удаляет сетевой интерфейс Azure.</span><span class="sxs-lookup"><span data-stu-id="471b6-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="471b6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="471b6-107">EXAMPLES</span></span>

### <span data-ttu-id="471b6-108">Пример 1. Удаление сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="471b6-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="471b6-109">Эта команда удаляет сетевой интерфейс NetworkInterface1 в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="471b6-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="471b6-110">Так как *параметр Force* не используется, пользователю будет предложено подтвердить это действие.</span><span class="sxs-lookup"><span data-stu-id="471b6-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="471b6-111">Пример 2. Удаление сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="471b6-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="471b6-112">Эта команда удаляет все сетевые интерфейсы группы ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="471b6-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="471b6-113">Так как используется параметр *Force,* пользователю не будет предложено подтверждение.</span><span class="sxs-lookup"><span data-stu-id="471b6-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="471b6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="471b6-114">PARAMETERS</span></span>

### <span data-ttu-id="471b6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="471b6-115">-AsJob</span></span>
<span data-ttu-id="471b6-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="471b6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="471b6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="471b6-117">-DefaultProfile</span></span>
<span data-ttu-id="471b6-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="471b6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="471b6-119">-Force</span><span class="sxs-lookup"><span data-stu-id="471b6-119">-Force</span></span>
<span data-ttu-id="471b6-120">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="471b6-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="471b6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="471b6-121">-Name</span></span>
<span data-ttu-id="471b6-122">Указывает имя сетевого интерфейса, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="471b6-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="471b6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="471b6-123">-PassThru</span></span>
<span data-ttu-id="471b6-124">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="471b6-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="471b6-125">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="471b6-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="471b6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="471b6-126">-ResourceGroupName</span></span>
<span data-ttu-id="471b6-127">Имя группы ресурсов, которая содержит сетевой интерфейс, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="471b6-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="471b6-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="471b6-128">-Confirm</span></span>
<span data-ttu-id="471b6-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="471b6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="471b6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="471b6-130">-WhatIf</span></span>
<span data-ttu-id="471b6-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="471b6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="471b6-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="471b6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="471b6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="471b6-133">CommonParameters</span></span>
<span data-ttu-id="471b6-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="471b6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="471b6-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="471b6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="471b6-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="471b6-136">INPUTS</span></span>

### <span data-ttu-id="471b6-137">System.String</span><span class="sxs-lookup"><span data-stu-id="471b6-137">System.String</span></span>

## <span data-ttu-id="471b6-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="471b6-138">OUTPUTS</span></span>

### <span data-ttu-id="471b6-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="471b6-139">System.Boolean</span></span>

## <span data-ttu-id="471b6-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="471b6-140">NOTES</span></span>

## <span data-ttu-id="471b6-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="471b6-141">RELATED LINKS</span></span>

[<span data-ttu-id="471b6-142">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="471b6-142">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="471b6-143">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="471b6-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="471b6-144">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="471b6-144">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


