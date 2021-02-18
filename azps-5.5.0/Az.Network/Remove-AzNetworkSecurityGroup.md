---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
ms.openlocfilehash: c5a5cbbbc46106fe6c388ee8f16117411f03fe0c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240661"
---
# <span data-ttu-id="5e37f-101">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5e37f-101">Remove-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="5e37f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e37f-102">SYNOPSIS</span></span>
<span data-ttu-id="5e37f-103">Удаляет группу безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="5e37f-103">Removes a network security group.</span></span>

## <span data-ttu-id="5e37f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5e37f-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e37f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e37f-105">DESCRIPTION</span></span>
<span data-ttu-id="5e37f-106">Командлет **Remove-AzNetworkSecurityGroup** удаляет группу безопасности сети Azure.</span><span class="sxs-lookup"><span data-stu-id="5e37f-106">The **Remove-AzNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="5e37f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5e37f-107">EXAMPLES</span></span>

### <span data-ttu-id="5e37f-108">Пример 1. Удаление группы безопасности сети</span><span class="sxs-lookup"><span data-stu-id="5e37f-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="5e37f-109">Эта команда удаляет группу безопасности с NSG-FrontEnd в группе ресурсов TestRG.</span><span class="sxs-lookup"><span data-stu-id="5e37f-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="5e37f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e37f-110">PARAMETERS</span></span>

### <span data-ttu-id="5e37f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e37f-111">-AsJob</span></span>
<span data-ttu-id="5e37f-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5e37f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e37f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e37f-113">-DefaultProfile</span></span>
<span data-ttu-id="5e37f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5e37f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e37f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5e37f-115">-Force</span></span>
<span data-ttu-id="5e37f-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="5e37f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5e37f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5e37f-117">-Name</span></span>
<span data-ttu-id="5e37f-118">Указывает имя группы безопасности сети, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e37f-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5e37f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e37f-119">-PassThru</span></span>
<span data-ttu-id="5e37f-120">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="5e37f-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5e37f-121">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5e37f-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5e37f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e37f-122">-ResourceGroupName</span></span>
<span data-ttu-id="5e37f-123">Имя группы ресурсов, из которого этот cmdlet удаляет группу безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="5e37f-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="5e37f-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e37f-124">-Confirm</span></span>
<span data-ttu-id="5e37f-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e37f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e37f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e37f-126">-WhatIf</span></span>
<span data-ttu-id="5e37f-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e37f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e37f-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5e37f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e37f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e37f-129">CommonParameters</span></span>
<span data-ttu-id="5e37f-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e37f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e37f-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e37f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e37f-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e37f-132">INPUTS</span></span>

### <span data-ttu-id="5e37f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5e37f-133">System.String</span></span>

## <span data-ttu-id="5e37f-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5e37f-134">OUTPUTS</span></span>

### <span data-ttu-id="5e37f-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5e37f-135">System.Boolean</span></span>

## <span data-ttu-id="5e37f-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5e37f-136">NOTES</span></span>

## <span data-ttu-id="5e37f-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e37f-137">RELATED LINKS</span></span>

[<span data-ttu-id="5e37f-138">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5e37f-138">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="5e37f-139">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5e37f-139">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="5e37f-140">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5e37f-140">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


