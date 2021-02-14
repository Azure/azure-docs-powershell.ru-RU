---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: b887110ecb0cd941af9c91417218ec2ca297be1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244093"
---
# <span data-ttu-id="7ef2d-101">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="7ef2d-101">Remove-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="7ef2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ef2d-102">SYNOPSIS</span></span>
<span data-ttu-id="7ef2d-103">Удаляет профиль пула агентов из службы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="7ef2d-103">Removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="7ef2d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7ef2d-104">SYNTAX</span></span>

```
Remove-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ef2d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ef2d-105">DESCRIPTION</span></span>
<span data-ttu-id="7ef2d-106">Для удаления профиля пула агентов из службы контейнера удаляется **cmdlet Remove-AzContainerServiceAgentPoolProfile.**</span><span class="sxs-lookup"><span data-stu-id="7ef2d-106">The **Remove-AzContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="7ef2d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7ef2d-107">EXAMPLES</span></span>

### <span data-ttu-id="7ef2d-108">Пример 1. Удаление профиля из службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="7ef2d-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="7ef2d-109">Первая команда получает службу контейнера CSResourceGroup17 с помощью Get-AzContainerService командлета.</span><span class="sxs-lookup"><span data-stu-id="7ef2d-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="7ef2d-110">Команда сохраняет службу в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="7ef2d-110">The command stores the service in the $Container variable.</span></span>
<span data-ttu-id="7ef2d-111">Вторая команда удаляет профиль AgentPool01 из службы контейнеров в $Container.</span><span class="sxs-lookup"><span data-stu-id="7ef2d-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="7ef2d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ef2d-112">PARAMETERS</span></span>

### <span data-ttu-id="7ef2d-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="7ef2d-113">-ContainerService</span></span>
<span data-ttu-id="7ef2d-114">Определяет объект службы контейнера, из которого этот cmdlet удаляет профиль пула агентов.</span><span class="sxs-lookup"><span data-stu-id="7ef2d-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

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

### <span data-ttu-id="7ef2d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ef2d-115">-DefaultProfile</span></span>
<span data-ttu-id="7ef2d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7ef2d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ef2d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7ef2d-117">-Name</span></span>
<span data-ttu-id="7ef2d-118">Указывает имя профиля пула агентов, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ef2d-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7ef2d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ef2d-119">-Confirm</span></span>
<span data-ttu-id="7ef2d-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7ef2d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ef2d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ef2d-121">-WhatIf</span></span>
<span data-ttu-id="7ef2d-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ef2d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ef2d-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7ef2d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ef2d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ef2d-124">CommonParameters</span></span>
<span data-ttu-id="7ef2d-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ef2d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ef2d-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ef2d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ef2d-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ef2d-127">INPUTS</span></span>

### <span data-ttu-id="7ef2d-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="7ef2d-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="7ef2d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="7ef2d-129">System.String</span></span>

## <span data-ttu-id="7ef2d-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7ef2d-130">OUTPUTS</span></span>

### <span data-ttu-id="7ef2d-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="7ef2d-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="7ef2d-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7ef2d-132">NOTES</span></span>

## <span data-ttu-id="7ef2d-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ef2d-133">RELATED LINKS</span></span>

[<span data-ttu-id="7ef2d-134">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="7ef2d-134">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="7ef2d-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="7ef2d-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)


