---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
ms.openlocfilehash: 2b102274b35d5f4f477376d3da8ad51bc6f0e694
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245584"
---
# <span data-ttu-id="e85bf-101">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="e85bf-101">Get-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="e85bf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e85bf-102">SYNOPSIS</span></span>
<span data-ttu-id="e85bf-103">Получает учетные данные для входа в реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="e85bf-103">Gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="e85bf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e85bf-104">SYNTAX</span></span>

### <span data-ttu-id="e85bf-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e85bf-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e85bf-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e85bf-106">RegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryCredential -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e85bf-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e85bf-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e85bf-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e85bf-108">DESCRIPTION</span></span>
<span data-ttu-id="e85bf-109">Командлет Get-AzContainerRegistryCredential получает учетные данные для входа в реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="e85bf-109">The Get-AzContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="e85bf-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e85bf-110">EXAMPLES</span></span>

### <span data-ttu-id="e85bf-111">Пример 1: получение учетных данных для входа в реестр контейнера</span><span class="sxs-lookup"><span data-stu-id="e85bf-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="e85bf-112">Эта команда получает учетные данные для входа в указанный контейнер реестра.</span><span class="sxs-lookup"><span data-stu-id="e85bf-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="e85bf-113">Чтобы \` получить учетные данные для входа, необходимо включить администратора в реестре MyRegistry \` .</span><span class="sxs-lookup"><span data-stu-id="e85bf-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="e85bf-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e85bf-114">PARAMETERS</span></span>

### <span data-ttu-id="e85bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e85bf-115">-DefaultProfile</span></span>
<span data-ttu-id="e85bf-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e85bf-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e85bf-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e85bf-117">-Name</span></span>
<span data-ttu-id="e85bf-118">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="e85bf-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="e85bf-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="e85bf-119">-Registry</span></span>
<span data-ttu-id="e85bf-120">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="e85bf-120">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e85bf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e85bf-121">-ResourceGroupName</span></span>
<span data-ttu-id="e85bf-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e85bf-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="e85bf-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e85bf-123">-ResourceId</span></span>
<span data-ttu-id="e85bf-124">Идентификатор ресурса реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="e85bf-124">The container registry resource id</span></span>

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

### <span data-ttu-id="e85bf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e85bf-125">CommonParameters</span></span>
<span data-ttu-id="e85bf-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e85bf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e85bf-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e85bf-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e85bf-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e85bf-128">INPUTS</span></span>

### <span data-ttu-id="e85bf-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e85bf-129">System.String</span></span>

## <span data-ttu-id="e85bf-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e85bf-130">OUTPUTS</span></span>

### <span data-ttu-id="e85bf-131">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="e85bf-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="e85bf-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="e85bf-132">NOTES</span></span>

## <span data-ttu-id="e85bf-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e85bf-133">RELATED LINKS</span></span>

[<span data-ttu-id="e85bf-134">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e85bf-134">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="e85bf-135">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e85bf-135">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="e85bf-136">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="e85bf-136">Update-AzContainerRegistryCredential</span></span>](Update-AzContainerRegistryCredential.md)
