---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 46eb802b4a91aa7ee7d370ed9ca93805497f21d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565544"
---
# <span data-ttu-id="be714-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="be714-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="be714-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be714-102">SYNOPSIS</span></span>
<span data-ttu-id="be714-103">Повторное создание учетных данных для входа в реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="be714-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be714-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be714-104">SYNTAX</span></span>

### <span data-ttu-id="be714-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="be714-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be714-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be714-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be714-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be714-107">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be714-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be714-108">DESCRIPTION</span></span>
<span data-ttu-id="be714-109">Командлет Update-AzureRmContainerRegistryCredential повторно генерирует учетные данные для входа в реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="be714-109">The Update-AzureRmContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="be714-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be714-110">EXAMPLES</span></span>

### <span data-ttu-id="be714-111">Пример 1: повторное создание учетных данных для входа в реестре контейнера</span><span class="sxs-lookup"><span data-stu-id="be714-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="be714-112">Эта команда повторно создает учетные данные для входа в указанный контейнер реестра.</span><span class="sxs-lookup"><span data-stu-id="be714-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="be714-113">Для \` \` повторного создания учетных данных в реестре MyRegistry пользователь администратора должен быть включен.</span><span class="sxs-lookup"><span data-stu-id="be714-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="be714-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be714-114">PARAMETERS</span></span>

### <span data-ttu-id="be714-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="be714-115">-Name</span></span>
<span data-ttu-id="be714-116">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="be714-116">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be714-117">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="be714-117">-PasswordName</span></span>
<span data-ttu-id="be714-118">Имя пароля, который нужно повторно создать.</span><span class="sxs-lookup"><span data-stu-id="be714-118">The name of password to regenerate.</span></span>
<span data-ttu-id="be714-119">Допустимые значения: Password, password2.</span><span class="sxs-lookup"><span data-stu-id="be714-119">Allowed values: password, password2.</span></span>

```yaml
Type: PasswordName
Parameter Sets: (All)
Aliases: 
Accepted values: Password, Password2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be714-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="be714-120">-Registry</span></span>
<span data-ttu-id="be714-121">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="be714-121">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be714-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be714-122">-ResourceGroupName</span></span>
<span data-ttu-id="be714-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="be714-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be714-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be714-124">-Confirm</span></span>
<span data-ttu-id="be714-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="be714-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be714-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be714-126">-WhatIf</span></span>
<span data-ttu-id="be714-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="be714-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be714-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="be714-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be714-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be714-129">-DefaultProfile</span></span>
<span data-ttu-id="be714-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="be714-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be714-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be714-131">-ResourceId</span></span>
<span data-ttu-id="be714-132">Идентификатор ресурса реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="be714-132">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be714-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be714-133">CommonParameters</span></span>
<span data-ttu-id="be714-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be714-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be714-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be714-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be714-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be714-136">INPUTS</span></span>

### <span data-ttu-id="be714-137">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="be714-137">PSContainerRegistry</span></span>
<span data-ttu-id="be714-138">Параметр "Registry" принимает значение типа "PSContainerRegistry" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="be714-138">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="be714-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be714-139">OUTPUTS</span></span>

### <span data-ttu-id="be714-140">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="be714-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="be714-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="be714-141">NOTES</span></span>

## <span data-ttu-id="be714-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be714-142">RELATED LINKS</span></span>

[<span data-ttu-id="be714-143">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="be714-143">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="be714-144">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="be714-144">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="be714-145">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="be714-145">Get-AzureRmContainerRegistryCredential</span></span>](Get-AzureRmContainerRegistryCredential.md)

