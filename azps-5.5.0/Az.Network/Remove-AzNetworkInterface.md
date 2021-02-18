---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: f4de49bb2e35bf3d392fba06d663800a5bdc44a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218345"
---
# <span data-ttu-id="ba4a4-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ba4a4-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="ba4a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba4a4-102">SYNOPSIS</span></span>
<span data-ttu-id="ba4a4-103">Удаляет сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-103">Removes a network interface.</span></span>

## <span data-ttu-id="ba4a4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ba4a4-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba4a4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba4a4-105">DESCRIPTION</span></span>
<span data-ttu-id="ba4a4-106">Командлет **Remove-AzNetworkInterface** удаляет сетевой интерфейс Azure.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="ba4a4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ba4a4-107">EXAMPLES</span></span>

### <span data-ttu-id="ba4a4-108">Пример 1. Удаление сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="ba4a4-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="ba4a4-109">Эта команда удаляет сетевой интерфейс NetworkInterface1 в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="ba4a4-110">Так как *параметр Force* не используется, пользователю будет предложено подтвердить это действие.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="ba4a4-111">Пример 2. Удаление сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="ba4a4-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="ba4a4-112">Эта команда удаляет все сетевые интерфейсы группы ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="ba4a4-113">Так как используется параметр *Force,* пользователю не будет предложено подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="ba4a4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba4a4-114">PARAMETERS</span></span>

### <span data-ttu-id="ba4a4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba4a4-115">-AsJob</span></span>
<span data-ttu-id="ba4a4-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ba4a4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ba4a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba4a4-117">-DefaultProfile</span></span>
<span data-ttu-id="ba4a4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba4a4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ba4a4-119">-Force</span></span>
<span data-ttu-id="ba4a4-120">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ba4a4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ba4a4-121">-Name</span></span>
<span data-ttu-id="ba4a4-122">Указывает имя сетевого интерфейса, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ba4a4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba4a4-123">-PassThru</span></span>
<span data-ttu-id="ba4a4-124">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ba4a4-125">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ba4a4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba4a4-126">-ResourceGroupName</span></span>
<span data-ttu-id="ba4a4-127">Имя группы ресурсов, которая содержит сетевой интерфейс, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ba4a4-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba4a4-128">-Confirm</span></span>
<span data-ttu-id="ba4a4-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba4a4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba4a4-130">-WhatIf</span></span>
<span data-ttu-id="ba4a4-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba4a4-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba4a4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba4a4-133">CommonParameters</span></span>
<span data-ttu-id="ba4a4-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba4a4-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba4a4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba4a4-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba4a4-136">INPUTS</span></span>

### <span data-ttu-id="ba4a4-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ba4a4-137">System.String</span></span>

## <span data-ttu-id="ba4a4-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ba4a4-138">OUTPUTS</span></span>

### <span data-ttu-id="ba4a4-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ba4a4-139">System.Boolean</span></span>

## <span data-ttu-id="ba4a4-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ba4a4-140">NOTES</span></span>

## <span data-ttu-id="ba4a4-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba4a4-141">RELATED LINKS</span></span>

[<span data-ttu-id="ba4a4-142">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ba4a4-142">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="ba4a4-143">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ba4a4-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="ba4a4-144">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ba4a4-144">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


