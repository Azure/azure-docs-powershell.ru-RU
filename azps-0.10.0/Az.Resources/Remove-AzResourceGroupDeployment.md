---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: da66d0cacbddbeb53972308faa681bde42c813d2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910842"
---
# <span data-ttu-id="f1965-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f1965-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="f1965-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1965-102">SYNOPSIS</span></span>
<span data-ttu-id="f1965-103">Удаляет развертывание группы ресурсов и связанные с ней операции.</span><span class="sxs-lookup"><span data-stu-id="f1965-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="f1965-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1965-104">SYNTAX</span></span>

### <span data-ttu-id="f1965-105">RemoveByResourceGroupName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f1965-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1965-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="f1965-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1965-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1965-107">DESCRIPTION</span></span>
<span data-ttu-id="f1965-108">Командлет **Remove-AzResourceGroupDeployment** удаляет развертывание группы ресурсов Azure и все связанные операции.</span><span class="sxs-lookup"><span data-stu-id="f1965-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="f1965-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1965-109">EXAMPLES</span></span>

## <span data-ttu-id="f1965-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1965-110">PARAMETERS</span></span>

### <span data-ttu-id="f1965-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f1965-111">-ApiVersion</span></span>
<span data-ttu-id="f1965-112">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f1965-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f1965-113">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f1965-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="f1965-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1965-114">-DefaultProfile</span></span>
<span data-ttu-id="f1965-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f1965-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1965-116">-ID</span><span class="sxs-lookup"><span data-stu-id="f1965-116">-Id</span></span>
<span data-ttu-id="f1965-117">Указывает идентификатор развертывания группы ресурсов, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="f1965-117">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="f1965-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f1965-118">-Name</span></span>
<span data-ttu-id="f1965-119">Указывает имя развертывания группы ресурсов, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="f1965-119">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="f1965-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="f1965-120">-Pre</span></span>
<span data-ttu-id="f1965-121">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="f1965-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f1965-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1965-122">-ResourceGroupName</span></span>
<span data-ttu-id="f1965-123">Указывает имя удаляемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f1965-123">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="f1965-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1965-124">-Confirm</span></span>
<span data-ttu-id="f1965-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f1965-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1965-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1965-126">-WhatIf</span></span>
<span data-ttu-id="f1965-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f1965-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1965-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f1965-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1965-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1965-129">CommonParameters</span></span>
<span data-ttu-id="f1965-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1965-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1965-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1965-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1965-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1965-132">INPUTS</span></span>

### <span data-ttu-id="f1965-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="f1965-133">None</span></span>

## <span data-ttu-id="f1965-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1965-134">OUTPUTS</span></span>

## <span data-ttu-id="f1965-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1965-135">NOTES</span></span>

## <span data-ttu-id="f1965-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1965-136">RELATED LINKS</span></span>

[<span data-ttu-id="f1965-137">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f1965-137">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="f1965-138">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f1965-138">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="f1965-139">Остановить-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f1965-139">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="f1965-140">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f1965-140">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


