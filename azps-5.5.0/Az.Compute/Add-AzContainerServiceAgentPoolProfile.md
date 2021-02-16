---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 8319a5bc0251e744ee898658b0a0a541f0ce86ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211852"
---
# <span data-ttu-id="12da0-101">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="12da0-101">Add-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="12da0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12da0-102">SYNOPSIS</span></span>
<span data-ttu-id="12da0-103">Добавляет профиль пула агентов службы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="12da0-103">Adds a container service agent pool profile.</span></span>

## <span data-ttu-id="12da0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="12da0-104">SYNTAX</span></span>

```
Add-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12da0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12da0-105">DESCRIPTION</span></span>
<span data-ttu-id="12da0-106">**Cmdlet Add-AzContainerServiceAgentPoolProfile** добавляет профиль агента контейнера в объект локальной службы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="12da0-106">The **Add-AzContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="12da0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="12da0-107">EXAMPLES</span></span>

### <span data-ttu-id="12da0-108">Пример 1. Добавление профиля</span><span class="sxs-lookup"><span data-stu-id="12da0-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="12da0-109">Эта команда добавляет профиль агента контейнера в объект локальной службы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="12da0-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="12da0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12da0-110">PARAMETERS</span></span>

### <span data-ttu-id="12da0-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="12da0-111">-ContainerService</span></span>
<span data-ttu-id="12da0-112">Определяет объект службы контейнера, к которому этот cmdlet добавляет профиль пула агентов.</span><span class="sxs-lookup"><span data-stu-id="12da0-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="12da0-113">Чтобы получить объект **ContainerService,** воспользуйтесь cmdlet [New-AzContainerServiceConfig.](./New-AzContainerServiceConfig.md)</span><span class="sxs-lookup"><span data-stu-id="12da0-113">To obtain a **ContainerService** object, use the [New-AzContainerServiceConfig](./New-AzContainerServiceConfig.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12da0-114">-Count</span><span class="sxs-lookup"><span data-stu-id="12da0-114">-Count</span></span>
<span data-ttu-id="12da0-115">Определяет количество агентов, которые могут контейнеры.</span><span class="sxs-lookup"><span data-stu-id="12da0-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="12da0-116">Допустимые значения этого параметра: от 1 до 100.</span><span class="sxs-lookup"><span data-stu-id="12da0-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="12da0-117">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="12da0-117">The default value is 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12da0-118">-DefaultProfile</span></span>
<span data-ttu-id="12da0-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="12da0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12da0-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="12da0-120">-DnsPrefix</span></span>
<span data-ttu-id="12da0-121">Указывает префикс DNS, который используется этим cmdlet для создания полного доменного имени для этого пула агентов.</span><span class="sxs-lookup"><span data-stu-id="12da0-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="12da0-122">-Name</span></span>
<span data-ttu-id="12da0-123">Указывает имя профиля пула агентов.</span><span class="sxs-lookup"><span data-stu-id="12da0-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="12da0-124">Это значение должно быть уникальным в контексте подписки и группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="12da0-124">This value must be unique in the context of the subscription and resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da0-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="12da0-125">-VmSize</span></span>
<span data-ttu-id="12da0-126">Определяет размер виртуальных машин для агентов.</span><span class="sxs-lookup"><span data-stu-id="12da0-126">Specifies the size of the virtual machines for the agents.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da0-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12da0-127">-Confirm</span></span>
<span data-ttu-id="12da0-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="12da0-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12da0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12da0-129">-WhatIf</span></span>
<span data-ttu-id="12da0-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12da0-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12da0-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="12da0-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12da0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12da0-132">CommonParameters</span></span>
<span data-ttu-id="12da0-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12da0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12da0-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12da0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12da0-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12da0-135">INPUTS</span></span>

### <span data-ttu-id="12da0-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="12da0-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="12da0-137">System.String</span><span class="sxs-lookup"><span data-stu-id="12da0-137">System.String</span></span>

### <span data-ttu-id="12da0-138">System.Int32</span><span class="sxs-lookup"><span data-stu-id="12da0-138">System.Int32</span></span>

## <span data-ttu-id="12da0-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="12da0-139">OUTPUTS</span></span>

### <span data-ttu-id="12da0-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="12da0-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="12da0-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="12da0-141">NOTES</span></span>

## <span data-ttu-id="12da0-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12da0-142">RELATED LINKS</span></span>

[<span data-ttu-id="12da0-143">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="12da0-143">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="12da0-144">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="12da0-144">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)
