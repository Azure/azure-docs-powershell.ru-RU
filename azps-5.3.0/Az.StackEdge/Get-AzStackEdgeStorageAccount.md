---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 59d01af85279414503b765aea7f326a8670ec1c2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504683"
---
# <span data-ttu-id="6feb8-101">Get-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6feb8-101">Get-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="6feb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6feb8-102">SYNOPSIS</span></span>
<span data-ttu-id="6feb8-103">Получает учетные записи edge Storage на устройстве.</span><span class="sxs-lookup"><span data-stu-id="6feb8-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="6feb8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6feb8-104">SYNTAX</span></span>

### <span data-ttu-id="6feb8-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6feb8-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6feb8-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6feb8-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6feb8-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6feb8-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6feb8-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6feb8-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="6feb8-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6feb8-109">DESCRIPTION</span></span>
<span data-ttu-id="6feb8-110">Для учетных записей Edge, доступных на устройстве Stack Edge, можно получить учетные записи **Get-AzStackEdgeStorageAccount.**</span><span class="sxs-lookup"><span data-stu-id="6feb8-110">The **Get-AzStackEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Stack Edge device.</span></span> <span data-ttu-id="6feb8-111">Вы можете указать имя в качестве параметра в cmdlet, чтобы получить сведения об определенной учетной записи edge Storage.</span><span class="sxs-lookup"><span data-stu-id="6feb8-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="6feb8-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6feb8-112">EXAMPLES</span></span>

### <span data-ttu-id="6feb8-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6feb8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="6feb8-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6feb8-114">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="6feb8-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6feb8-115">Example 3</span></span>
```powershell
PS C:\> Get-AzStackEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzStackEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="6feb8-116">Пример 4</span><span class="sxs-lookup"><span data-stu-id="6feb8-116">Example 4</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="6feb8-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6feb8-117">PARAMETERS</span></span>

### <span data-ttu-id="6feb8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6feb8-118">-DefaultProfile</span></span>
<span data-ttu-id="6feb8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6feb8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6feb8-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6feb8-120">-DeviceName</span></span>
<span data-ttu-id="6feb8-121">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="6feb8-121">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6feb8-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="6feb8-122">-DeviceObject</span></span>
<span data-ttu-id="6feb8-123">Предосообщите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="6feb8-123">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6feb8-124">-Name</span><span class="sxs-lookup"><span data-stu-id="6feb8-124">-Name</span></span>
<span data-ttu-id="6feb8-125">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="6feb8-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageAccountName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6feb8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6feb8-126">-ResourceGroupName</span></span>
<span data-ttu-id="6feb8-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6feb8-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6feb8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6feb8-128">-ResourceId</span></span>
<span data-ttu-id="6feb8-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6feb8-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6feb8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6feb8-130">CommonParameters</span></span>
<span data-ttu-id="6feb8-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6feb8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6feb8-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6feb8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6feb8-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6feb8-133">INPUTS</span></span>

### <span data-ttu-id="6feb8-134">System.String</span><span class="sxs-lookup"><span data-stu-id="6feb8-134">System.String</span></span>

### <span data-ttu-id="6feb8-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="6feb8-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="6feb8-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6feb8-136">OUTPUTS</span></span>

### <span data-ttu-id="6feb8-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6feb8-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="6feb8-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6feb8-138">NOTES</span></span>

## <span data-ttu-id="6feb8-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6feb8-139">RELATED LINKS</span></span>
