---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
ms.openlocfilehash: d8e5f36366df16dd7b0d03fb07f948e436c0a919
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079078"
---
# <span data-ttu-id="a5055-101">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="a5055-101">Update-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="a5055-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a5055-102">SYNOPSIS</span></span>
<span data-ttu-id="a5055-103">Повторное создание учетных данных для входа в реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="a5055-103">Regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="a5055-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a5055-104">SYNTAX</span></span>

### <span data-ttu-id="a5055-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a5055-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5055-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5055-106">RegistryObjectParameterSet</span></span>
```
Update-AzContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5055-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5055-107">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5055-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5055-108">DESCRIPTION</span></span>
<span data-ttu-id="a5055-109">Командлет Update-AzContainerRegistryCredential повторно генерирует учетные данные для входа в реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="a5055-109">The Update-AzContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="a5055-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a5055-110">EXAMPLES</span></span>

### <span data-ttu-id="a5055-111">Пример 1: повторное создание учетных данных для входа в реестре контейнера</span><span class="sxs-lookup"><span data-stu-id="a5055-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="a5055-112">Эта команда повторно создает учетные данные для входа в указанный контейнер реестра.</span><span class="sxs-lookup"><span data-stu-id="a5055-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="a5055-113">Для \` \` повторного создания учетных данных в реестре MyRegistry пользователь администратора должен быть включен.</span><span class="sxs-lookup"><span data-stu-id="a5055-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="a5055-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a5055-114">PARAMETERS</span></span>

### <span data-ttu-id="a5055-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5055-115">-DefaultProfile</span></span>
<span data-ttu-id="a5055-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a5055-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5055-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a5055-117">-Name</span></span>
<span data-ttu-id="a5055-118">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="a5055-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="a5055-119">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="a5055-119">-PasswordName</span></span>
<span data-ttu-id="a5055-120">Имя пароля, который нужно повторно создать.</span><span class="sxs-lookup"><span data-stu-id="a5055-120">The name of password to regenerate.</span></span>
<span data-ttu-id="a5055-121">Допустимые значения: Password, password2.</span><span class="sxs-lookup"><span data-stu-id="a5055-121">Allowed values: password, password2.</span></span>

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

### <span data-ttu-id="a5055-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="a5055-122">-Registry</span></span>
<span data-ttu-id="a5055-123">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="a5055-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="a5055-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5055-124">-ResourceGroupName</span></span>
<span data-ttu-id="a5055-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a5055-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a5055-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5055-126">-ResourceId</span></span>
<span data-ttu-id="a5055-127">Идентификатор ресурса реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="a5055-127">The container registry resource id</span></span>

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

### <span data-ttu-id="a5055-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5055-128">-Confirm</span></span>
<span data-ttu-id="a5055-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a5055-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5055-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5055-130">-WhatIf</span></span>
<span data-ttu-id="a5055-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a5055-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5055-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a5055-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5055-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5055-133">CommonParameters</span></span>
<span data-ttu-id="a5055-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a5055-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5055-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5055-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5055-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a5055-136">INPUTS</span></span>

### <span data-ttu-id="a5055-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a5055-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="a5055-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a5055-138">System.String</span></span>

## <span data-ttu-id="a5055-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5055-139">OUTPUTS</span></span>

### <span data-ttu-id="a5055-140">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="a5055-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="a5055-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="a5055-141">NOTES</span></span>

## <span data-ttu-id="a5055-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5055-142">RELATED LINKS</span></span>

[<span data-ttu-id="a5055-143">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a5055-143">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="a5055-144">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a5055-144">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="a5055-145">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="a5055-145">Get-AzContainerRegistryCredential</span></span>](Get-AzContainerRegistryCredential.md)
