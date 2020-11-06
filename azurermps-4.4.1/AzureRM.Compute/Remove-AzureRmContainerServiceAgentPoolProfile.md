---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 355938c64926d0c97d7e1393abd5c8a0d5ce20ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568802"
---
# <span data-ttu-id="8e805-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="8e805-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="8e805-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e805-102">SYNOPSIS</span></span>
<span data-ttu-id="8e805-103">Удаляет профиль пула агентов из службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="8e805-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e805-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e805-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e805-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e805-105">DESCRIPTION</span></span>
<span data-ttu-id="8e805-106">Командлет **Remove-AzureRmContainerServiceAgentPoolProfile** удаляет профиль пула агентов из службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="8e805-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="8e805-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e805-107">EXAMPLES</span></span>

### <span data-ttu-id="8e805-108">Пример 1: Удаление профиля из службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="8e805-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="8e805-109">Первая команда получает службу контейнеров с именем CSResourceGroup17 с помощью командлета Get-AzureRmContainerService.</span><span class="sxs-lookup"><span data-stu-id="8e805-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="8e805-110">Команда хранит службу в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="8e805-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="8e805-111">Вторая команда удаляет профиль с именем AgentPool01 из службы контейнера в $Container.</span><span class="sxs-lookup"><span data-stu-id="8e805-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="8e805-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e805-112">PARAMETERS</span></span>

### <span data-ttu-id="8e805-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="8e805-113">-ContainerService</span></span>
<span data-ttu-id="8e805-114">Указывает объект службы контейнера, из которого этот командлет удаляет профиль пула агентов.</span><span class="sxs-lookup"><span data-stu-id="8e805-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

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

### <span data-ttu-id="8e805-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e805-115">-DefaultProfile</span></span>
<span data-ttu-id="8e805-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e805-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e805-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8e805-117">-Name</span></span>
<span data-ttu-id="8e805-118">Указывает имя профиля пула агентов, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="8e805-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8e805-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e805-119">-Confirm</span></span>
<span data-ttu-id="8e805-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8e805-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e805-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e805-121">-WhatIf</span></span>
<span data-ttu-id="8e805-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8e805-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e805-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8e805-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e805-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e805-124">CommonParameters</span></span>
<span data-ttu-id="8e805-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e805-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e805-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e805-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e805-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e805-127">INPUTS</span></span>

## <span data-ttu-id="8e805-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e805-128">OUTPUTS</span></span>

## <span data-ttu-id="8e805-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e805-129">NOTES</span></span>

## <span data-ttu-id="8e805-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e805-130">RELATED LINKS</span></span>

[<span data-ttu-id="8e805-131">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="8e805-131">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="8e805-132">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="8e805-132">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)


