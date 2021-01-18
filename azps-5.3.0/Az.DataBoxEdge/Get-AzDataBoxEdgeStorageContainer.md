---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 3f7ebc42efc2ad5ba73079fd2774614b941f432b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519101"
---
# <span data-ttu-id="5dccd-101">Get-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="5dccd-101">Get-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="5dccd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dccd-102">SYNOPSIS</span></span>
<span data-ttu-id="5dccd-103">Контейнеры для учетной записи edge Storage на устройстве.</span><span class="sxs-lookup"><span data-stu-id="5dccd-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="5dccd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5dccd-104">SYNTAX</span></span>

### <span data-ttu-id="5dccd-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5dccd-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5dccd-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dccd-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5dccd-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dccd-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5dccd-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dccd-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSDataBoxEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="5dccd-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5dccd-109">DESCRIPTION</span></span>
<span data-ttu-id="5dccd-110">На **устройстве Edge Data Box** можно получить контейнер хранилища для учетной записи Edge Storage.</span><span class="sxs-lookup"><span data-stu-id="5dccd-110">The **Get-AzDataBoxEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="5dccd-111">Вы можете указать имя в качестве параметра в cmdlet, чтобы получить сведения об определенном контейнере хранилища.</span><span class="sxs-lookup"><span data-stu-id="5dccd-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="5dccd-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5dccd-112">EXAMPLES</span></span>

### <span data-ttu-id="5dccd-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5dccd-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="5dccd-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5dccd-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="5dccd-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5dccd-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount | Get-AzDataBoxEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="5dccd-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5dccd-116">PARAMETERS</span></span>

### <span data-ttu-id="5dccd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dccd-117">-DefaultProfile</span></span>
<span data-ttu-id="5dccd-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5dccd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dccd-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5dccd-119">-DeviceName</span></span>
<span data-ttu-id="5dccd-120">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="5dccd-120">Device Name</span></span>

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

### <span data-ttu-id="5dccd-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5dccd-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="5dccd-122">Укайм существующее имя EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5dccd-122">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dccd-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="5dccd-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="5dccd-124">Предоставление существующего объекта EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5dccd-124">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5dccd-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5dccd-125">-Name</span></span>
<span data-ttu-id="5dccd-126">Имя edgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="5dccd-126">Name of the EdgeStorageContainer</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageContainerName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dccd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dccd-127">-ResourceGroupName</span></span>
<span data-ttu-id="5dccd-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5dccd-128">Resource Group Name</span></span>

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

### <span data-ttu-id="5dccd-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5dccd-129">-ResourceId</span></span>
<span data-ttu-id="5dccd-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5dccd-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dccd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dccd-131">CommonParameters</span></span>
<span data-ttu-id="5dccd-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dccd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dccd-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5dccd-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dccd-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5dccd-134">INPUTS</span></span>

### <span data-ttu-id="5dccd-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5dccd-135">System.String</span></span>

### <span data-ttu-id="5dccd-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5dccd-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="5dccd-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5dccd-137">OUTPUTS</span></span>

### <span data-ttu-id="5dccd-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="5dccd-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="5dccd-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5dccd-139">NOTES</span></span>

## <span data-ttu-id="5dccd-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5dccd-140">RELATED LINKS</span></span>
