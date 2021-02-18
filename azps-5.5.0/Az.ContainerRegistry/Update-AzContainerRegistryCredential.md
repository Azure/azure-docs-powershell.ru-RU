---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
ms.openlocfilehash: d8e5f36366df16dd7b0d03fb07f948e436c0a919
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215484"
---
# <span data-ttu-id="23198-101">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="23198-101">Update-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="23198-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23198-102">SYNOPSIS</span></span>
<span data-ttu-id="23198-103">Повторное сгенерирует учетные данные для реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="23198-103">Regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="23198-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="23198-104">SYNTAX</span></span>

### <span data-ttu-id="23198-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23198-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23198-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23198-106">RegistryObjectParameterSet</span></span>
```
Update-AzContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23198-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23198-107">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23198-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23198-108">DESCRIPTION</span></span>
<span data-ttu-id="23198-109">При Update-AzContainerRegistryCredential-за этого будет повторно сгенерироваться учетные данные для входа в реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="23198-109">The Update-AzContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="23198-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="23198-110">EXAMPLES</span></span>

### <span data-ttu-id="23198-111">Пример 1. Повторное сгенерировать учетные данные для реестра контейнеров</span><span class="sxs-lookup"><span data-stu-id="23198-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="23198-112">Эта команда повторно определяет учетные данные для указанного реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="23198-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="23198-113">Пользователю администратора необходимо включить реестр контейнера MyRegistry для повторного сгенерации \` \` учетных данных для входа.</span><span class="sxs-lookup"><span data-stu-id="23198-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="23198-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23198-114">PARAMETERS</span></span>

### <span data-ttu-id="23198-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23198-115">-DefaultProfile</span></span>
<span data-ttu-id="23198-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="23198-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23198-117">-Name</span><span class="sxs-lookup"><span data-stu-id="23198-117">-Name</span></span>
<span data-ttu-id="23198-118">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="23198-118">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23198-119">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="23198-119">-PasswordName</span></span>
<span data-ttu-id="23198-120">Имя пароля для повторного сгенерации.</span><span class="sxs-lookup"><span data-stu-id="23198-120">The name of password to regenerate.</span></span>
<span data-ttu-id="23198-121">Разрешенные значения: password, password2.</span><span class="sxs-lookup"><span data-stu-id="23198-121">Allowed values: password, password2.</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerRegistry.Models.PasswordName
Parameter Sets: (All)
Aliases:
Accepted values: password, password2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23198-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="23198-122">-Registry</span></span>
<span data-ttu-id="23198-123">Объект Container Registry.</span><span class="sxs-lookup"><span data-stu-id="23198-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23198-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23198-124">-ResourceGroupName</span></span>
<span data-ttu-id="23198-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23198-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23198-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23198-126">-ResourceId</span></span>
<span data-ttu-id="23198-127">ИД контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="23198-127">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23198-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23198-128">-Confirm</span></span>
<span data-ttu-id="23198-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23198-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23198-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23198-130">-WhatIf</span></span>
<span data-ttu-id="23198-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23198-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23198-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="23198-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23198-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23198-133">CommonParameters</span></span>
<span data-ttu-id="23198-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23198-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23198-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23198-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23198-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23198-136">INPUTS</span></span>

### <span data-ttu-id="23198-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="23198-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="23198-138">System.String</span><span class="sxs-lookup"><span data-stu-id="23198-138">System.String</span></span>

## <span data-ttu-id="23198-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="23198-139">OUTPUTS</span></span>

### <span data-ttu-id="23198-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="23198-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="23198-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="23198-141">NOTES</span></span>

## <span data-ttu-id="23198-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23198-142">RELATED LINKS</span></span>

[<span data-ttu-id="23198-143">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="23198-143">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="23198-144">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="23198-144">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="23198-145">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="23198-145">Get-AzContainerRegistryCredential</span></span>](Get-AzContainerRegistryCredential.md)

