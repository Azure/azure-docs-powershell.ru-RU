---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 9a199a0aa0e31cf8bc57585d4825a33e10b5bfc1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915334"
---
# <span data-ttu-id="74cdd-101">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="74cdd-101">Update-AzureRmContainerService</span></span>

## <span data-ttu-id="74cdd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74cdd-102">SYNOPSIS</span></span>
<span data-ttu-id="74cdd-103">Обновляет состояние службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="74cdd-103">Updates the state of a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74cdd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74cdd-104">SYNTAX</span></span>

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74cdd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74cdd-105">DESCRIPTION</span></span>
<span data-ttu-id="74cdd-106">Командлет **Update-AzureRmContainerService** обновляет состояние службы контейнеров в соответствии с локальным экземпляром службы.</span><span class="sxs-lookup"><span data-stu-id="74cdd-106">The **Update-AzureRmContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="74cdd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74cdd-107">EXAMPLES</span></span>

### <span data-ttu-id="74cdd-108">Пример 1: обновление службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="74cdd-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="74cdd-109">Эта команда получает службу контейнеров с именем CSResourceGroup17 с помощью командлета Get-AzureRmContainerService.</span><span class="sxs-lookup"><span data-stu-id="74cdd-109">This command gets the container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="74cdd-110">Команда передает этот объект в командлет Remove-AzureRmContainerServiceAgentPoolProfile с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="74cdd-110">The command passes that object to the Remove-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="74cdd-111">**Remove-AzureRmContainerServiceAgentPoolProfile** удаляет профиль с именем AgentPool01.</span><span class="sxs-lookup"><span data-stu-id="74cdd-111">**Remove-AzureRmContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="74cdd-112">Команда передает результат в командлет Add-AzureRmContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="74cdd-112">The command passes the result to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

<span data-ttu-id="74cdd-113">**Add-AzureRmContainerServiceAgentPoolProfile** добавляет профиль с именем AgentPool01 и имеет указанные свойства.</span><span class="sxs-lookup"><span data-stu-id="74cdd-113">**Add-AzureRmContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="74cdd-114">Команда передает результат в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="74cdd-114">The command passes the result to the current cmdlet.</span></span>

<span data-ttu-id="74cdd-115">Текущий командлет обновляет службу контейнеров, чтобы отразить изменения, внесенные в этой команде.</span><span class="sxs-lookup"><span data-stu-id="74cdd-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="74cdd-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74cdd-116">PARAMETERS</span></span>

### <span data-ttu-id="74cdd-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74cdd-117">-AsJob</span></span>
<span data-ttu-id="74cdd-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="74cdd-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74cdd-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="74cdd-119">-ContainerService</span></span>
<span data-ttu-id="74cdd-120">Указывает локальный объект **ContainerService** , который содержит изменения.</span><span class="sxs-lookup"><span data-stu-id="74cdd-120">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74cdd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74cdd-121">-DefaultProfile</span></span>
<span data-ttu-id="74cdd-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74cdd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74cdd-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="74cdd-123">-Name</span></span>
<span data-ttu-id="74cdd-124">Указывает имя службы контейнера, которая обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="74cdd-124">Specifies the name of the container service that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74cdd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74cdd-125">-ResourceGroupName</span></span>
<span data-ttu-id="74cdd-126">Указывает группу ресурсов службы контейнера, которая обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="74cdd-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="74cdd-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74cdd-127">-Confirm</span></span>
<span data-ttu-id="74cdd-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="74cdd-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74cdd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74cdd-129">-WhatIf</span></span>
<span data-ttu-id="74cdd-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="74cdd-130">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="74cdd-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="74cdd-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74cdd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74cdd-132">CommonParameters</span></span>
<span data-ttu-id="74cdd-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74cdd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74cdd-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74cdd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74cdd-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74cdd-135">INPUTS</span></span>

### <span data-ttu-id="74cdd-136">ContainerService</span><span class="sxs-lookup"><span data-stu-id="74cdd-136">ContainerService</span></span>
<span data-ttu-id="74cdd-137">Параметр "ContainerService" принимает значение типа "ContainerService" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="74cdd-137">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="74cdd-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74cdd-138">OUTPUTS</span></span>

### <span data-ttu-id="74cdd-139">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="74cdd-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="74cdd-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="74cdd-140">NOTES</span></span>

## <span data-ttu-id="74cdd-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74cdd-141">RELATED LINKS</span></span>

[<span data-ttu-id="74cdd-142">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="74cdd-142">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="74cdd-143">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="74cdd-143">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="74cdd-144">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="74cdd-144">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="74cdd-145">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="74cdd-145">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="74cdd-146">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="74cdd-146">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)


