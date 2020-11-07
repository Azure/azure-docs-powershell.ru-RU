---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerserviceagentpoolprofile
schema: 2.0.0
ms.openlocfilehash: 2bbc7d9e1ac125134931be483d3a693252ce12d0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914553"
---
# <span data-ttu-id="af067-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="af067-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="af067-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af067-102">SYNOPSIS</span></span>
<span data-ttu-id="af067-103">Удаляет профиль пула агентов из службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="af067-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af067-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af067-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af067-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af067-105">DESCRIPTION</span></span>
<span data-ttu-id="af067-106">Командлет **Remove-AzureRmContainerServiceAgentPoolProfile** удаляет профиль пула агентов из службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="af067-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="af067-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af067-107">EXAMPLES</span></span>

### <span data-ttu-id="af067-108">Пример 1: Удаление профиля из службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="af067-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="af067-109">Первая команда получает службу контейнеров с именем CSResourceGroup17 с помощью командлета Get-AzureRmContainerService.</span><span class="sxs-lookup"><span data-stu-id="af067-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="af067-110">Команда хранит службу в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="af067-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="af067-111">Вторая команда удаляет профиль с именем AgentPool01 из службы контейнера в $Container.</span><span class="sxs-lookup"><span data-stu-id="af067-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="af067-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af067-112">PARAMETERS</span></span>

### <span data-ttu-id="af067-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="af067-113">-ContainerService</span></span>
<span data-ttu-id="af067-114">Указывает объект службы контейнера, из которого этот командлет удаляет профиль пула агентов.</span><span class="sxs-lookup"><span data-stu-id="af067-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af067-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af067-115">-DefaultProfile</span></span>
<span data-ttu-id="af067-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af067-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af067-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="af067-117">-Name</span></span>
<span data-ttu-id="af067-118">Указывает имя профиля пула агентов, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="af067-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af067-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af067-119">-Confirm</span></span>
<span data-ttu-id="af067-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="af067-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af067-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af067-121">-WhatIf</span></span>
<span data-ttu-id="af067-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="af067-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af067-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="af067-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af067-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af067-124">CommonParameters</span></span>
<span data-ttu-id="af067-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af067-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af067-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af067-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af067-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af067-127">INPUTS</span></span>

### <span data-ttu-id="af067-128">ContainerService</span><span class="sxs-lookup"><span data-stu-id="af067-128">ContainerService</span></span>
<span data-ttu-id="af067-129">Параметр "ContainerService" принимает значение типа "ContainerService" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="af067-129">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="af067-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af067-130">OUTPUTS</span></span>

### <span data-ttu-id="af067-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="af067-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="af067-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="af067-132">NOTES</span></span>

## <span data-ttu-id="af067-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af067-133">RELATED LINKS</span></span>

[<span data-ttu-id="af067-134">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="af067-134">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="af067-135">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="af067-135">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)


