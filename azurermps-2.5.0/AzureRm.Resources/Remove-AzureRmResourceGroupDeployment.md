---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: bfe0bad0104708e635b49f02cfb1eecd2474ea5b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915001"
---
# <span data-ttu-id="9dde7-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9dde7-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="9dde7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9dde7-102">SYNOPSIS</span></span>
<span data-ttu-id="9dde7-103">Удаляет развертывание группы ресурсов и связанные с ней операции.</span><span class="sxs-lookup"><span data-stu-id="9dde7-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9dde7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9dde7-104">SYNTAX</span></span>

### <span data-ttu-id="9dde7-105">RemoveByResourceGroupName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9dde7-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dde7-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="9dde7-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dde7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dde7-107">DESCRIPTION</span></span>
<span data-ttu-id="9dde7-108">Командлет **Remove-AzureRmResourceGroupDeployment** удаляет развертывание группы ресурсов Azure и все связанные операции.</span><span class="sxs-lookup"><span data-stu-id="9dde7-108">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="9dde7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9dde7-109">EXAMPLES</span></span>

## <span data-ttu-id="9dde7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9dde7-110">PARAMETERS</span></span>

### <span data-ttu-id="9dde7-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9dde7-111">-ApiVersion</span></span>
<span data-ttu-id="9dde7-112">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9dde7-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="9dde7-113">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9dde7-113">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dde7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dde7-114">-DefaultProfile</span></span>
<span data-ttu-id="9dde7-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9dde7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9dde7-116">-ID</span><span class="sxs-lookup"><span data-stu-id="9dde7-116">-Id</span></span>
<span data-ttu-id="9dde7-117">Указывает идентификатор развертывания группы ресурсов, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="9dde7-117">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dde7-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9dde7-118">-Name</span></span>
<span data-ttu-id="9dde7-119">Указывает имя развертывания группы ресурсов, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="9dde7-119">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dde7-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="9dde7-120">-Pre</span></span>
<span data-ttu-id="9dde7-121">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="9dde7-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dde7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dde7-122">-ResourceGroupName</span></span>
<span data-ttu-id="9dde7-123">Указывает имя удаляемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9dde7-123">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dde7-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9dde7-124">-Confirm</span></span>
<span data-ttu-id="9dde7-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9dde7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dde7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dde7-126">-WhatIf</span></span>
<span data-ttu-id="9dde7-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9dde7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dde7-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9dde7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dde7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dde7-129">CommonParameters</span></span>
<span data-ttu-id="9dde7-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9dde7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dde7-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dde7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dde7-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9dde7-132">INPUTS</span></span>

### <span data-ttu-id="9dde7-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="9dde7-133">None</span></span>

## <span data-ttu-id="9dde7-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dde7-134">OUTPUTS</span></span>

## <span data-ttu-id="9dde7-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="9dde7-135">NOTES</span></span>

## <span data-ttu-id="9dde7-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9dde7-136">RELATED LINKS</span></span>

[<span data-ttu-id="9dde7-137">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9dde7-137">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="9dde7-138">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9dde7-138">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="9dde7-139">Остановить-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9dde7-139">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="9dde7-140">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9dde7-140">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


