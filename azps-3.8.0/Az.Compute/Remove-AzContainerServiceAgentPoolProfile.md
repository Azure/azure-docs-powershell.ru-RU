---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: b887110ecb0cd941af9c91417218ec2ca297be1c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93913063"
---
# <span data-ttu-id="62793-101">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="62793-101">Remove-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="62793-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62793-102">SYNOPSIS</span></span>
<span data-ttu-id="62793-103">Удаляет профиль пула агентов из службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="62793-103">Removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="62793-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62793-104">SYNTAX</span></span>

```
Remove-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62793-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62793-105">DESCRIPTION</span></span>
<span data-ttu-id="62793-106">Командлет **Remove-AzContainerServiceAgentPoolProfile** удаляет профиль пула агентов из службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="62793-106">The **Remove-AzContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="62793-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62793-107">EXAMPLES</span></span>

### <span data-ttu-id="62793-108">Пример 1: Удаление профиля из службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="62793-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="62793-109">Первая команда получает службу контейнеров с именем CSResourceGroup17 с помощью командлета Get-AzContainerService.</span><span class="sxs-lookup"><span data-stu-id="62793-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="62793-110">Команда хранит службу в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="62793-110">The command stores the service in the $Container variable.</span></span>
<span data-ttu-id="62793-111">Вторая команда удаляет профиль с именем AgentPool01 из службы контейнера в $Container.</span><span class="sxs-lookup"><span data-stu-id="62793-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="62793-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62793-112">PARAMETERS</span></span>

### <span data-ttu-id="62793-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="62793-113">-ContainerService</span></span>
<span data-ttu-id="62793-114">Указывает объект службы контейнера, из которого этот командлет удаляет профиль пула агентов.</span><span class="sxs-lookup"><span data-stu-id="62793-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

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

### <span data-ttu-id="62793-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62793-115">-DefaultProfile</span></span>
<span data-ttu-id="62793-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62793-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62793-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="62793-117">-Name</span></span>
<span data-ttu-id="62793-118">Указывает имя профиля пула агентов, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="62793-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="62793-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62793-119">-Confirm</span></span>
<span data-ttu-id="62793-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="62793-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62793-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62793-121">-WhatIf</span></span>
<span data-ttu-id="62793-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="62793-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62793-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="62793-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62793-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62793-124">CommonParameters</span></span>
<span data-ttu-id="62793-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62793-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62793-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62793-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62793-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62793-127">INPUTS</span></span>

### <span data-ttu-id="62793-128">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="62793-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="62793-129">System. String</span><span class="sxs-lookup"><span data-stu-id="62793-129">System.String</span></span>

## <span data-ttu-id="62793-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62793-130">OUTPUTS</span></span>

### <span data-ttu-id="62793-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="62793-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="62793-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="62793-132">NOTES</span></span>

## <span data-ttu-id="62793-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62793-133">RELATED LINKS</span></span>

[<span data-ttu-id="62793-134">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="62793-134">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="62793-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="62793-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)


