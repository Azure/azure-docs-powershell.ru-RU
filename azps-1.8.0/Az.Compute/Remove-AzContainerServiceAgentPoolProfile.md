---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: dc1884d643bd2f3c58ae6cb68fe272a786bcde73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901222"
---
# <span data-ttu-id="f2007-101">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="f2007-101">Remove-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="f2007-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2007-102">SYNOPSIS</span></span>
<span data-ttu-id="f2007-103">Удаляет профиль пула агентов из службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="f2007-103">Removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="f2007-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2007-104">SYNTAX</span></span>

```
Remove-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2007-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2007-105">DESCRIPTION</span></span>
<span data-ttu-id="f2007-106">Командлет **Remove-AzContainerServiceAgentPoolProfile** удаляет профиль пула агентов из службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="f2007-106">The **Remove-AzContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="f2007-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2007-107">EXAMPLES</span></span>

### <span data-ttu-id="f2007-108">Пример 1: Удаление профиля из службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="f2007-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="f2007-109">Первая команда получает службу контейнеров с именем CSResourceGroup17 с помощью командлета Get-AzContainerService.</span><span class="sxs-lookup"><span data-stu-id="f2007-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="f2007-110">Команда хранит службу в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="f2007-110">The command stores the service in the $Container variable.</span></span>
<span data-ttu-id="f2007-111">Вторая команда удаляет профиль с именем AgentPool01 из службы контейнера в $Container.</span><span class="sxs-lookup"><span data-stu-id="f2007-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="f2007-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2007-112">PARAMETERS</span></span>

### <span data-ttu-id="f2007-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="f2007-113">-ContainerService</span></span>
<span data-ttu-id="f2007-114">Указывает объект службы контейнера, из которого этот командлет удаляет профиль пула агентов.</span><span class="sxs-lookup"><span data-stu-id="f2007-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

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

### <span data-ttu-id="f2007-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2007-115">-DefaultProfile</span></span>
<span data-ttu-id="f2007-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2007-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2007-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f2007-117">-Name</span></span>
<span data-ttu-id="f2007-118">Указывает имя профиля пула агентов, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="f2007-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2007-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2007-119">-Confirm</span></span>
<span data-ttu-id="f2007-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f2007-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2007-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2007-121">-WhatIf</span></span>
<span data-ttu-id="f2007-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f2007-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2007-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f2007-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2007-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2007-124">CommonParameters</span></span>
<span data-ttu-id="f2007-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2007-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2007-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2007-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2007-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2007-127">INPUTS</span></span>

### <span data-ttu-id="f2007-128">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="f2007-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="f2007-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f2007-129">System.String</span></span>

## <span data-ttu-id="f2007-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2007-130">OUTPUTS</span></span>

### <span data-ttu-id="f2007-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="f2007-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="f2007-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2007-132">NOTES</span></span>

## <span data-ttu-id="f2007-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2007-133">RELATED LINKS</span></span>

[<span data-ttu-id="f2007-134">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="f2007-134">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="f2007-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="f2007-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)


