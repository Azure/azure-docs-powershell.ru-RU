---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
ms.openlocfilehash: 4e937bd3ec1c40aaf4b3c1c188b157792c0030bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903442"
---
# <span data-ttu-id="6f075-101">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6f075-101">Remove-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="6f075-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f075-102">SYNOPSIS</span></span>
<span data-ttu-id="6f075-103">Удаляет сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="6f075-103">Removes a network security group.</span></span>

## <span data-ttu-id="6f075-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f075-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f075-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f075-105">DESCRIPTION</span></span>
<span data-ttu-id="6f075-106">Командлет **Remove-AzNetworkSecurityGroup** удаляет сетевую группу безопасности Azure.</span><span class="sxs-lookup"><span data-stu-id="6f075-106">The **Remove-AzNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="6f075-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f075-107">EXAMPLES</span></span>

### <span data-ttu-id="6f075-108">Пример 1: Удаление группы безопасности сети</span><span class="sxs-lookup"><span data-stu-id="6f075-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="6f075-109">Эта команда удаляет группу безопасности с именем NSG-FrontEnd в группе ресурсов с именем TestRG.</span><span class="sxs-lookup"><span data-stu-id="6f075-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="6f075-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f075-110">PARAMETERS</span></span>

### <span data-ttu-id="6f075-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f075-111">-AsJob</span></span>
<span data-ttu-id="6f075-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6f075-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f075-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f075-113">-DefaultProfile</span></span>
<span data-ttu-id="6f075-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f075-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f075-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6f075-115">-Force</span></span>
<span data-ttu-id="6f075-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="6f075-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6f075-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6f075-117">-Name</span></span>
<span data-ttu-id="6f075-118">Указывает имя сетевой группы безопасности, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6f075-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6f075-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f075-119">-PassThru</span></span>
<span data-ttu-id="6f075-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="6f075-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6f075-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6f075-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6f075-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f075-122">-ResourceGroupName</span></span>
<span data-ttu-id="6f075-123">Указывает имя группы ресурсов, из которой этот командлет удаляет сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="6f075-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="6f075-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f075-124">-Confirm</span></span>
<span data-ttu-id="6f075-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6f075-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f075-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f075-126">-WhatIf</span></span>
<span data-ttu-id="6f075-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6f075-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f075-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6f075-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f075-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f075-129">CommonParameters</span></span>
<span data-ttu-id="6f075-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f075-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f075-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f075-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f075-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f075-132">INPUTS</span></span>

### <span data-ttu-id="6f075-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6f075-133">System.String</span></span>

## <span data-ttu-id="6f075-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f075-134">OUTPUTS</span></span>

### <span data-ttu-id="6f075-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f075-135">System.Boolean</span></span>

## <span data-ttu-id="6f075-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f075-136">NOTES</span></span>

## <span data-ttu-id="6f075-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f075-137">RELATED LINKS</span></span>

[<span data-ttu-id="6f075-138">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6f075-138">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="6f075-139">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6f075-139">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="6f075-140">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6f075-140">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


