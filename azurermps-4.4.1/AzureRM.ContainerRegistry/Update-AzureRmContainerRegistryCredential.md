---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: e65367a94e946aee83df2087463bd0081e925862
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732707"
---
# <span data-ttu-id="84417-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="84417-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="84417-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="84417-102">SYNOPSIS</span></span>
<span data-ttu-id="84417-103">Повторное создание учетных данных для входа в реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="84417-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84417-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="84417-104">SYNTAX</span></span>

### <span data-ttu-id="84417-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="84417-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84417-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84417-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84417-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84417-107">DESCRIPTION</span></span>
<span data-ttu-id="84417-108">Командлет **Update-AzureRmContainerRegistryCredential** заново генерирует учетные данные для входа в реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="84417-108">The **Update-AzureRmContainerRegistryCredential** cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="84417-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="84417-109">EXAMPLES</span></span>

### <span data-ttu-id="84417-110">Пример 1: повторное создание учетных данных для входа в реестре контейнера</span><span class="sxs-lookup"><span data-stu-id="84417-110">Example 1: Regenerate a login credential for a container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="84417-111">Эта команда повторно создает учетные данные для входа в указанный контейнер реестра.</span><span class="sxs-lookup"><span data-stu-id="84417-111">This command regenerates a login credential for the specified container registry.</span></span> <span data-ttu-id="84417-112">Для повторного создания учетных данных пользователя администратору необходимо включить в реестре контейнера `MyRegistry` .</span><span class="sxs-lookup"><span data-stu-id="84417-112">Admin user has to be enabled for the container registry `MyRegistry` to regenerate login credentials.</span></span>

## <span data-ttu-id="84417-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="84417-113">PARAMETERS</span></span>

### <span data-ttu-id="84417-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="84417-114">-Name</span></span>
<span data-ttu-id="84417-115">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="84417-115">Container Registry Name.</span></span>

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

### <span data-ttu-id="84417-116">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="84417-116">-PasswordName</span></span>
<span data-ttu-id="84417-117">Имя пароля, который нужно повторно создать.</span><span class="sxs-lookup"><span data-stu-id="84417-117">The name of password to regenerate.</span></span>
<span data-ttu-id="84417-118">Допустимые значения: Password, password2.</span><span class="sxs-lookup"><span data-stu-id="84417-118">Allowed values: password, password2.</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerRegistry.Models.PasswordName
Parameter Sets: (All)
Aliases: 
Accepted values: Password, Password2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84417-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="84417-119">-Registry</span></span>
<span data-ttu-id="84417-120">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="84417-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="84417-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84417-121">-ResourceGroupName</span></span>
<span data-ttu-id="84417-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="84417-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="84417-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84417-123">-Confirm</span></span>
<span data-ttu-id="84417-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="84417-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84417-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84417-125">-WhatIf</span></span>
<span data-ttu-id="84417-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="84417-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84417-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="84417-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84417-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84417-128">-DefaultProfile</span></span>
<span data-ttu-id="84417-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84417-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84417-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84417-130">CommonParameters</span></span>
<span data-ttu-id="84417-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="84417-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84417-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84417-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84417-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="84417-133">INPUTS</span></span>

### <span data-ttu-id="84417-134">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="84417-134">PSContainerRegistry</span></span>
<span data-ttu-id="84417-135">Параметр "Registry" принимает значение типа "PSContainerRegistry" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="84417-135">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="84417-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="84417-136">OUTPUTS</span></span>

### <span data-ttu-id="84417-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="84417-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="84417-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="84417-138">NOTES</span></span>

## <span data-ttu-id="84417-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84417-139">RELATED LINKS</span></span>

[<span data-ttu-id="84417-140">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="84417-140">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="84417-141">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="84417-141">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="84417-142">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="84417-142">Get-AzureRmContainerRegistryCredential</span></span>](./Get-AzureRmContainerRegistryCredential.md)

