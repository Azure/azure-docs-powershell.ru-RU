---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
ms.openlocfilehash: d7f494b6ba943214106363a5b7dfe4dfb5cdd877
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078567"
---
# <span data-ttu-id="afb0c-101">Get-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="afb0c-101">Get-AzSynapseLinkedService</span></span>

## <span data-ttu-id="afb0c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="afb0c-102">SYNOPSIS</span></span>
<span data-ttu-id="afb0c-103">Получение сведений о связанных службах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="afb0c-103">Gets information about linked services in workspace.</span></span>

## <span data-ttu-id="afb0c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="afb0c-104">SYNTAX</span></span>

### <span data-ttu-id="afb0c-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="afb0c-105">GetByName (Default)</span></span>
```
Get-AzSynapseLinkedService -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="afb0c-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="afb0c-106">GetByObject</span></span>
```
Get-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afb0c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="afb0c-107">DESCRIPTION</span></span>
<span data-ttu-id="afb0c-108">Командлет **Get-AzSynapseLinkedService** получает сведения о связанных службах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="afb0c-108">The **Get-AzSynapseLinkedService** cmdlet gets information about linked services in workspace.</span></span>
<span data-ttu-id="afb0c-109">Если указать имя связанной службы, этот командлет получает сведения о связанной службе.</span><span class="sxs-lookup"><span data-stu-id="afb0c-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="afb0c-110">Если имя не задано, этот командлет получает сведения обо всех связанных службах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="afb0c-110">If you do not specify a name, this cmdlet gets information about all the linked services in the workspace.</span></span>

## <span data-ttu-id="afb0c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="afb0c-111">EXAMPLES</span></span>

### <span data-ttu-id="afb0c-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="afb0c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="afb0c-113">Эта команда получает сведения обо всех связанных службах в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="afb0c-113">This command gets information about all linked services in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="afb0c-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="afb0c-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="afb0c-115">Эта команда получает сведения о связанной службе с именем ContosoLinkedService в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="afb0c-115">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="afb0c-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="afb0c-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="afb0c-117">Эта команда получает сведения о связанной службе с именем ContosoLinkedService в рабочей области с именем ContosoWorkspace с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="afb0c-117">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="afb0c-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="afb0c-118">PARAMETERS</span></span>

### <span data-ttu-id="afb0c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afb0c-119">-DefaultProfile</span></span>
<span data-ttu-id="afb0c-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="afb0c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afb0c-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="afb0c-121">-Name</span></span>
<span data-ttu-id="afb0c-122">Имя связанной службы.</span><span class="sxs-lookup"><span data-stu-id="afb0c-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afb0c-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="afb0c-123">-WorkspaceName</span></span>
<span data-ttu-id="afb0c-124">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="afb0c-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afb0c-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="afb0c-125">-WorkspaceObject</span></span>
<span data-ttu-id="afb0c-126">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="afb0c-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afb0c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb0c-127">CommonParameters</span></span>
<span data-ttu-id="afb0c-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="afb0c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb0c-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="afb0c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb0c-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="afb0c-130">INPUTS</span></span>

### <span data-ttu-id="afb0c-131">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="afb0c-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="afb0c-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="afb0c-132">OUTPUTS</span></span>

### <span data-ttu-id="afb0c-133">Microsoft. Azure. Commands. Synapse. Models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="afb0c-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="afb0c-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="afb0c-134">NOTES</span></span>

## <span data-ttu-id="afb0c-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="afb0c-135">RELATED LINKS</span></span>
