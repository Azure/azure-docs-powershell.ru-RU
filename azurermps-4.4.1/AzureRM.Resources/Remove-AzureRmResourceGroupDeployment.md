---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 84aa6f50d02f4c85de674c163565a205f2b83750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567060"
---
# <span data-ttu-id="84322-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="84322-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="84322-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="84322-102">SYNOPSIS</span></span>
<span data-ttu-id="84322-103">Удаляет развертывание группы ресурсов и связанные с ней операции.</span><span class="sxs-lookup"><span data-stu-id="84322-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84322-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="84322-104">SYNTAX</span></span>

### <span data-ttu-id="84322-105">Заданный параметр имени развертывания.</span><span class="sxs-lookup"><span data-stu-id="84322-105">The deployment name parameter set.</span></span> <span data-ttu-id="84322-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="84322-106">(Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84322-107">Заданный параметр идентификатора развертывания.</span><span class="sxs-lookup"><span data-stu-id="84322-107">The deployment Id parameter set.</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84322-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84322-108">DESCRIPTION</span></span>
<span data-ttu-id="84322-109">Командлет **Remove-AzureRmResourceGroupDeployment** удаляет развертывание группы ресурсов Azure и все связанные операции.</span><span class="sxs-lookup"><span data-stu-id="84322-109">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="84322-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="84322-110">EXAMPLES</span></span>

## <span data-ttu-id="84322-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="84322-111">PARAMETERS</span></span>

### <span data-ttu-id="84322-112">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="84322-112">-ApiVersion</span></span>
<span data-ttu-id="84322-113">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="84322-113">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="84322-114">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84322-114">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="84322-115">-ID</span><span class="sxs-lookup"><span data-stu-id="84322-115">-Id</span></span>
<span data-ttu-id="84322-116">Указывает идентификатор развертывания группы ресурсов, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="84322-116">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment Id parameter set.
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84322-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="84322-117">-Name</span></span>
<span data-ttu-id="84322-118">Указывает имя развертывания группы ресурсов, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="84322-118">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84322-119">-Pre</span><span class="sxs-lookup"><span data-stu-id="84322-119">-Pre</span></span>
<span data-ttu-id="84322-120">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="84322-120">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="84322-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84322-121">-ResourceGroupName</span></span>
<span data-ttu-id="84322-122">Указывает имя удаляемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="84322-122">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84322-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84322-123">-Confirm</span></span>
<span data-ttu-id="84322-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="84322-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84322-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84322-125">-WhatIf</span></span>
<span data-ttu-id="84322-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="84322-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84322-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="84322-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84322-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84322-128">-DefaultProfile</span></span>
<span data-ttu-id="84322-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84322-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84322-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84322-130">CommonParameters</span></span>
<span data-ttu-id="84322-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="84322-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84322-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84322-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84322-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="84322-133">INPUTS</span></span>

## <span data-ttu-id="84322-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="84322-134">OUTPUTS</span></span>

### <span data-ttu-id="84322-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="84322-135">System.Boolean</span></span>

## <span data-ttu-id="84322-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="84322-136">NOTES</span></span>

## <span data-ttu-id="84322-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84322-137">RELATED LINKS</span></span>

[<span data-ttu-id="84322-138">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="84322-138">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="84322-139">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="84322-139">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="84322-140">Остановить-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="84322-140">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="84322-141">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="84322-141">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


