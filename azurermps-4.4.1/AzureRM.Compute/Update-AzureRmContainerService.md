---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmContainerService.md
ms.openlocfilehash: ca6a89f7818760a6bab65e45fec703c00d8e7f8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569599"
---
# <span data-ttu-id="68db5-101">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="68db5-101">Update-AzureRmContainerService</span></span>

## <span data-ttu-id="68db5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="68db5-102">SYNOPSIS</span></span>
<span data-ttu-id="68db5-103">Обновляет состояние службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="68db5-103">Updates the state of a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68db5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="68db5-104">SYNTAX</span></span>

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68db5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68db5-105">DESCRIPTION</span></span>
<span data-ttu-id="68db5-106">Командлет **Update-AzureRmContainerService** обновляет состояние службы контейнеров в соответствии с локальным экземпляром службы.</span><span class="sxs-lookup"><span data-stu-id="68db5-106">The **Update-AzureRmContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="68db5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="68db5-107">EXAMPLES</span></span>

### <span data-ttu-id="68db5-108">Пример 1: обновление службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="68db5-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="68db5-109">Эта команда получает службу контейнеров с именем CSResourceGroup17 с помощью командлета Get-AzureRmContainerService.</span><span class="sxs-lookup"><span data-stu-id="68db5-109">This command gets the container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="68db5-110">Команда передает этот объект в командлет Remove-AzureRmContainerServiceAgentPoolProfile с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="68db5-110">The command passes that object to the Remove-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="68db5-111">**Remove-AzureRmContainerServiceAgentPoolProfile** удаляет профиль с именем AgentPool01.</span><span class="sxs-lookup"><span data-stu-id="68db5-111">**Remove-AzureRmContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="68db5-112">Команда передает результат в командлет Add-AzureRmContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="68db5-112">The command passes the result to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

<span data-ttu-id="68db5-113">**Add-AzureRmContainerServiceAgentPoolProfile** добавляет профиль с именем AgentPool01 и имеет указанные свойства.</span><span class="sxs-lookup"><span data-stu-id="68db5-113">**Add-AzureRmContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="68db5-114">Команда передает результат в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="68db5-114">The command passes the result to the current cmdlet.</span></span>

<span data-ttu-id="68db5-115">Текущий командлет обновляет службу контейнеров, чтобы отразить изменения, внесенные в этой команде.</span><span class="sxs-lookup"><span data-stu-id="68db5-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="68db5-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="68db5-116">PARAMETERS</span></span>

### <span data-ttu-id="68db5-117">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="68db5-117">-ContainerService</span></span>
<span data-ttu-id="68db5-118">Указывает локальный объект **ContainerService** , который содержит изменения.</span><span class="sxs-lookup"><span data-stu-id="68db5-118">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68db5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68db5-119">-DefaultProfile</span></span>
<span data-ttu-id="68db5-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="68db5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68db5-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="68db5-121">-Name</span></span>
<span data-ttu-id="68db5-122">Указывает имя службы контейнера, которая обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="68db5-122">Specifies the name of the container service that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68db5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68db5-123">-ResourceGroupName</span></span>
<span data-ttu-id="68db5-124">Указывает группу ресурсов службы контейнера, которая обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="68db5-124">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="68db5-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68db5-125">-Confirm</span></span>
<span data-ttu-id="68db5-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="68db5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68db5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68db5-127">-WhatIf</span></span>
<span data-ttu-id="68db5-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="68db5-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="68db5-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="68db5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68db5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68db5-130">CommonParameters</span></span>
<span data-ttu-id="68db5-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="68db5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68db5-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68db5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68db5-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="68db5-133">INPUTS</span></span>

## <span data-ttu-id="68db5-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="68db5-134">OUTPUTS</span></span>

## <span data-ttu-id="68db5-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="68db5-135">NOTES</span></span>

## <span data-ttu-id="68db5-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68db5-136">RELATED LINKS</span></span>

[<span data-ttu-id="68db5-137">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="68db5-137">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="68db5-138">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="68db5-138">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="68db5-139">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="68db5-139">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="68db5-140">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="68db5-140">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="68db5-141">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="68db5-141">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)


