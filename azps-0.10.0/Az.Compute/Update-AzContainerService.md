---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzContainerService.md
ms.openlocfilehash: 1a15486b3e24dec3af66cb98391bd8322c28d2e6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910451"
---
# <span data-ttu-id="aec36-101">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="aec36-101">Update-AzContainerService</span></span>

## <span data-ttu-id="aec36-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aec36-102">SYNOPSIS</span></span>
<span data-ttu-id="aec36-103">Обновляет состояние службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="aec36-103">Updates the state of a container service.</span></span>

## <span data-ttu-id="aec36-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aec36-104">SYNTAX</span></span>

```
Update-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aec36-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aec36-105">DESCRIPTION</span></span>
<span data-ttu-id="aec36-106">Командлет **Update-AzContainerService** обновляет состояние службы контейнеров в соответствии с локальным экземпляром службы.</span><span class="sxs-lookup"><span data-stu-id="aec36-106">The **Update-AzContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="aec36-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aec36-107">EXAMPLES</span></span>

### <span data-ttu-id="aec36-108">Пример 1: обновление службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="aec36-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="aec36-109">Эта команда получает службу контейнеров с именем CSResourceGroup17 с помощью командлета Get-AzContainerService.</span><span class="sxs-lookup"><span data-stu-id="aec36-109">This command gets the container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="aec36-110">Команда передает этот объект в командлет Remove-AzContainerServiceAgentPoolProfile с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="aec36-110">The command passes that object to the Remove-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="aec36-111">**Remove-AzContainerServiceAgentPoolProfile** удаляет профиль с именем AgentPool01.</span><span class="sxs-lookup"><span data-stu-id="aec36-111">**Remove-AzContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="aec36-112">Команда передает результат в командлет Add-AzContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="aec36-112">The command passes the result to the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>

<span data-ttu-id="aec36-113">**Add-AzContainerServiceAgentPoolProfile** добавляет профиль с именем AgentPool01 и имеет указанные свойства.</span><span class="sxs-lookup"><span data-stu-id="aec36-113">**Add-AzContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="aec36-114">Команда передает результат в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="aec36-114">The command passes the result to the current cmdlet.</span></span>

<span data-ttu-id="aec36-115">Текущий командлет обновляет службу контейнеров, чтобы отразить изменения, внесенные в этой команде.</span><span class="sxs-lookup"><span data-stu-id="aec36-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="aec36-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aec36-116">PARAMETERS</span></span>

### <span data-ttu-id="aec36-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aec36-117">-AsJob</span></span>
<span data-ttu-id="aec36-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="aec36-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aec36-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="aec36-119">-ContainerService</span></span>
<span data-ttu-id="aec36-120">Указывает локальный объект **ContainerService** , который содержит изменения.</span><span class="sxs-lookup"><span data-stu-id="aec36-120">Specifies a local **ContainerService** object that contains changes.</span></span>

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

### <span data-ttu-id="aec36-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aec36-121">-DefaultProfile</span></span>
<span data-ttu-id="aec36-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aec36-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aec36-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aec36-123">-Name</span></span>
<span data-ttu-id="aec36-124">Указывает имя службы контейнера, которая обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="aec36-124">Specifies the name of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="aec36-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aec36-125">-ResourceGroupName</span></span>
<span data-ttu-id="aec36-126">Указывает группу ресурсов службы контейнера, которая обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="aec36-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="aec36-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aec36-127">-Confirm</span></span>
<span data-ttu-id="aec36-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aec36-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aec36-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aec36-129">-WhatIf</span></span>
<span data-ttu-id="aec36-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aec36-130">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="aec36-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aec36-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aec36-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aec36-132">CommonParameters</span></span>
<span data-ttu-id="aec36-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aec36-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aec36-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aec36-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aec36-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aec36-135">INPUTS</span></span>

### <span data-ttu-id="aec36-136">ContainerService</span><span class="sxs-lookup"><span data-stu-id="aec36-136">ContainerService</span></span>
<span data-ttu-id="aec36-137">Параметр "ContainerService" принимает значение типа "ContainerService" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="aec36-137">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="aec36-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aec36-138">OUTPUTS</span></span>

### <span data-ttu-id="aec36-139">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="aec36-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="aec36-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="aec36-140">NOTES</span></span>

## <span data-ttu-id="aec36-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aec36-141">RELATED LINKS</span></span>

[<span data-ttu-id="aec36-142">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="aec36-142">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="aec36-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="aec36-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="aec36-144">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="aec36-144">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="aec36-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="aec36-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="aec36-146">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="aec36-146">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)


