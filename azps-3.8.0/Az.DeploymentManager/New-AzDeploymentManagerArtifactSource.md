---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: dcd8d4164d091564aef3d3802430ab499eac38ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074388"
---
# <span data-ttu-id="28eb1-101">New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="28eb1-101">New-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="28eb1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="28eb1-103">Создание источника артефактов.</span><span class="sxs-lookup"><span data-stu-id="28eb1-103">Creates an artifact source.</span></span>

## <span data-ttu-id="28eb1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28eb1-104">SYNTAX</span></span>

```
New-AzDeploymentManagerArtifactSource -ResourceGroupName <String> -Name <String> -Location <String>
 -SasUri <String> [-Tag <Hashtable>] [-ArtifactRoot <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28eb1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28eb1-105">DESCRIPTION</span></span>
<span data-ttu-id="28eb1-106">Командлет **New-AzDeploymentManagerArtifactSource** создает источник артефакта.</span><span class="sxs-lookup"><span data-stu-id="28eb1-106">The **New-AzDeploymentManagerArtifactSource** cmdlet creates an artifact source.</span></span>
<span data-ttu-id="28eb1-107">Укажите *имя* , *ResourceGroupName* и необходимые свойства.</span><span class="sxs-lookup"><span data-stu-id="28eb1-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="28eb1-108">Вы можете изменить возвращаемый объект на локальном компьютере, а затем применить изменения к источнику артефакта с помощью командлета Set-AzDeploymentManagerArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="28eb1-108">You can modify the returned object locally and then apply the changes to the artifact source by using the Set-AzDeploymentManagerArtifactSource cmdlet.</span></span>

<span data-ttu-id="28eb1-109">Командлет возвращает объект ArtifactSource, у которого есть ResourceId, на который можно ссылаться в командлете New-AzDeploymentManagerServiceTopology, так что артефакты, необходимые для ресурса ServiceUnit, Template и файлов параметров, могут ссылаться из этого места.</span><span class="sxs-lookup"><span data-stu-id="28eb1-109">The cmdlet returns an ArtifactSource object that has a ResourceId which can be referenced in the New-AzDeploymentManagerServiceTopology cmdlet so that artifacts required for a ServiceUnit resource, the Template and Parameters files, can be referenced from this location.</span></span>

## <span data-ttu-id="28eb1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28eb1-110">EXAMPLES</span></span>

### <span data-ttu-id="28eb1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="28eb1-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerArtifactSource -ResourceGroupName ContosoResourceGroup -Name ContosoArtifactSource -Location "Central US" -SasUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts?sasParameters"
```

<span data-ttu-id="28eb1-112">Создает источник артефактов в ContosoResourceGroup с именем ContosoArtifactSource, где в качестве местоположения ресурса указан центральный элемент US.</span><span class="sxs-lookup"><span data-stu-id="28eb1-112">Creates an artifact source in the ContosoResourceGroup with the name ContosoArtifactSource with Central US as the location of the resource.</span></span> <span data-ttu-id="28eb1-113">Свойство SasUri предоставляет универсальный код ресурса SAS хранилища Azure для контейнера хранилища, в котором хранятся артефакты.</span><span class="sxs-lookup"><span data-stu-id="28eb1-113">The SasUri property provides an Azure Storage SAS Uri to the storage container where the artifacts are stored.</span></span>

## <span data-ttu-id="28eb1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28eb1-114">PARAMETERS</span></span>

### <span data-ttu-id="28eb1-115">-ArtifactRoot</span><span class="sxs-lookup"><span data-stu-id="28eb1-115">-ArtifactRoot</span></span>
<span data-ttu-id="28eb1-116">Необязательное смещение каталога в контейнере хранения для артефактов.</span><span class="sxs-lookup"><span data-stu-id="28eb1-116">The optional directory offset under the storage container for the artifacts.</span></span>

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

### <span data-ttu-id="28eb1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28eb1-117">-DefaultProfile</span></span>
<span data-ttu-id="28eb1-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28eb1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28eb1-119">-Location</span><span class="sxs-lookup"><span data-stu-id="28eb1-119">-Location</span></span>
<span data-ttu-id="28eb1-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="28eb1-120">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28eb1-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="28eb1-121">-Name</span></span>
<span data-ttu-id="28eb1-122">Имя источника артефакта.</span><span class="sxs-lookup"><span data-stu-id="28eb1-122">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28eb1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28eb1-123">-ResourceGroupName</span></span>
<span data-ttu-id="28eb1-124">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="28eb1-124">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28eb1-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="28eb1-125">-SasUri</span></span>
<span data-ttu-id="28eb1-126">Универсальный код ресурса (URI) SAS для контейнера хранилища Azure, в котором хранятся артефакты.</span><span class="sxs-lookup"><span data-stu-id="28eb1-126">The SAS Uri to the Azure storage container where the artifacts are stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28eb1-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="28eb1-127">-Tag</span></span>
<span data-ttu-id="28eb1-128">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="28eb1-128">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28eb1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28eb1-129">-Confirm</span></span>
<span data-ttu-id="28eb1-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="28eb1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28eb1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28eb1-131">-WhatIf</span></span>
<span data-ttu-id="28eb1-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="28eb1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28eb1-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="28eb1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28eb1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28eb1-134">CommonParameters</span></span>
<span data-ttu-id="28eb1-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28eb1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28eb1-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28eb1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28eb1-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28eb1-137">INPUTS</span></span>

### <span data-ttu-id="28eb1-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="28eb1-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="28eb1-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28eb1-139">OUTPUTS</span></span>

### <span data-ttu-id="28eb1-140">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="28eb1-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="28eb1-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="28eb1-141">NOTES</span></span>

## <span data-ttu-id="28eb1-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28eb1-142">RELATED LINKS</span></span>
