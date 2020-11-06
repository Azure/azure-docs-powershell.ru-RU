---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: a5ce087e8ebf768b63d09a4002c3aaf38ddd9f84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569676"
---
# <span data-ttu-id="924e3-101">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="924e3-101">Add-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="924e3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="924e3-102">SYNOPSIS</span></span>
<span data-ttu-id="924e3-103">Добавляет профиль пула агента службы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="924e3-103">Adds a container service agent pool profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="924e3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="924e3-104">SYNTAX</span></span>

```
Add-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="924e3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="924e3-105">DESCRIPTION</span></span>
<span data-ttu-id="924e3-106">Командлет **Add-AzureRmContainerServiceAgentPoolProfile** добавляет профиль пула агента службы контейнеров в локальный объект службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="924e3-106">The **Add-AzureRmContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="924e3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="924e3-107">EXAMPLES</span></span>

### <span data-ttu-id="924e3-108">Пример 1: Добавление профиля</span><span class="sxs-lookup"><span data-stu-id="924e3-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="924e3-109">Эта команда добавляет профиль пула агента службы контейнеров в локальный объект службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="924e3-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="924e3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="924e3-110">PARAMETERS</span></span>

### <span data-ttu-id="924e3-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="924e3-111">-ContainerService</span></span>
<span data-ttu-id="924e3-112">Указывает объект службы контейнера, к которому этот командлет добавляет профиль пула агентов.</span><span class="sxs-lookup"><span data-stu-id="924e3-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="924e3-113">Чтобы получить объект **ContainerService** , используйте командлет [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="924e3-113">To obtain a **ContainerService** object, use the [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="924e3-114">— Количество</span><span class="sxs-lookup"><span data-stu-id="924e3-114">-Count</span></span>
<span data-ttu-id="924e3-115">Указывает количество агентов, которые размещает контейнеры.</span><span class="sxs-lookup"><span data-stu-id="924e3-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="924e3-116">Допустимые значения этого параметра: целые числа от 1 до 100.</span><span class="sxs-lookup"><span data-stu-id="924e3-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="924e3-117">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="924e3-117">The default value is 1.</span></span>

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

### <span data-ttu-id="924e3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="924e3-118">-DefaultProfile</span></span>
<span data-ttu-id="924e3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="924e3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="924e3-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="924e3-120">-DnsPrefix</span></span>
<span data-ttu-id="924e3-121">Указывает префикс DNS, используемый этим командлетом для создания полного доменного имени для этого пула агентов.</span><span class="sxs-lookup"><span data-stu-id="924e3-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

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

### <span data-ttu-id="924e3-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="924e3-122">-Name</span></span>
<span data-ttu-id="924e3-123">Указывает имя профиля пула агентов.</span><span class="sxs-lookup"><span data-stu-id="924e3-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="924e3-124">Это значение должно быть уникальным в контексте подписки и группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="924e3-124">This value must be unique in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="924e3-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="924e3-125">-VmSize</span></span>
<span data-ttu-id="924e3-126">Указывает размер виртуальных машин для агентов.</span><span class="sxs-lookup"><span data-stu-id="924e3-126">Specifies the size of the virtual machines for the agents.</span></span>

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

### <span data-ttu-id="924e3-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="924e3-127">-Confirm</span></span>
<span data-ttu-id="924e3-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="924e3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="924e3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="924e3-129">-WhatIf</span></span>
<span data-ttu-id="924e3-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="924e3-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="924e3-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="924e3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="924e3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="924e3-132">CommonParameters</span></span>
<span data-ttu-id="924e3-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="924e3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="924e3-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="924e3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="924e3-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="924e3-135">INPUTS</span></span>

## <span data-ttu-id="924e3-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="924e3-136">OUTPUTS</span></span>

## <span data-ttu-id="924e3-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="924e3-137">NOTES</span></span>

## <span data-ttu-id="924e3-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="924e3-138">RELATED LINKS</span></span>

[<span data-ttu-id="924e3-139">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="924e3-139">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="924e3-140">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="924e3-140">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)
