---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 836e8983a9d2e6c7ff21444f0da7b3bf85c1b1d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568929"
---
# <span data-ttu-id="35794-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="35794-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="35794-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35794-102">SYNOPSIS</span></span>
<span data-ttu-id="35794-103">Повторное создание учетных данных для входа в реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="35794-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35794-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35794-104">SYNTAX</span></span>

### <span data-ttu-id="35794-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35794-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35794-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35794-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35794-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35794-107">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35794-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35794-108">DESCRIPTION</span></span>
<span data-ttu-id="35794-109">Командлет Update-AzureRmContainerRegistryCredential повторно генерирует учетные данные для входа в реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="35794-109">The Update-AzureRmContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="35794-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35794-110">EXAMPLES</span></span>

### <span data-ttu-id="35794-111">Пример 1: повторное создание учетных данных для входа в реестре контейнера</span><span class="sxs-lookup"><span data-stu-id="35794-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="35794-112">Эта команда повторно создает учетные данные для входа в указанный контейнер реестра.</span><span class="sxs-lookup"><span data-stu-id="35794-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="35794-113">Для \` \` повторного создания учетных данных в реестре MyRegistry пользователь администратора должен быть включен.</span><span class="sxs-lookup"><span data-stu-id="35794-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="35794-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35794-114">PARAMETERS</span></span>

### <span data-ttu-id="35794-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35794-115">-DefaultProfile</span></span>
<span data-ttu-id="35794-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="35794-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35794-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="35794-117">-Name</span></span>
<span data-ttu-id="35794-118">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="35794-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="35794-119">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="35794-119">-PasswordName</span></span>
<span data-ttu-id="35794-120">Имя пароля, который нужно повторно создать.</span><span class="sxs-lookup"><span data-stu-id="35794-120">The name of password to regenerate.</span></span>
<span data-ttu-id="35794-121">Допустимые значения: Password, password2.</span><span class="sxs-lookup"><span data-stu-id="35794-121">Allowed values: password, password2.</span></span>

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

### <span data-ttu-id="35794-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="35794-122">-Registry</span></span>
<span data-ttu-id="35794-123">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="35794-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="35794-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35794-124">-ResourceGroupName</span></span>
<span data-ttu-id="35794-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35794-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="35794-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35794-126">-ResourceId</span></span>
<span data-ttu-id="35794-127">Идентификатор ресурса реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="35794-127">The container registry resource id</span></span>

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

### <span data-ttu-id="35794-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35794-128">-Confirm</span></span>
<span data-ttu-id="35794-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="35794-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35794-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35794-130">-WhatIf</span></span>
<span data-ttu-id="35794-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="35794-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35794-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="35794-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35794-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35794-133">CommonParameters</span></span>
<span data-ttu-id="35794-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35794-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35794-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35794-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35794-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35794-136">INPUTS</span></span>

### <span data-ttu-id="35794-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="35794-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="35794-138">Параметры: Registry (ByValue)</span><span class="sxs-lookup"><span data-stu-id="35794-138">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="35794-139">System. String</span><span class="sxs-lookup"><span data-stu-id="35794-139">System.String</span></span>

## <span data-ttu-id="35794-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35794-140">OUTPUTS</span></span>

### <span data-ttu-id="35794-141">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="35794-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="35794-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="35794-142">NOTES</span></span>

## <span data-ttu-id="35794-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35794-143">RELATED LINKS</span></span>

[<span data-ttu-id="35794-144">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="35794-144">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="35794-145">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="35794-145">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="35794-146">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="35794-146">Get-AzureRmContainerRegistryCredential</span></span>](Get-AzureRmContainerRegistryCredential.md)

