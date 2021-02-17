---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 0b18183b27f5701036afb74bb85768b48e9492e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217305"
---
# <span data-ttu-id="d214d-101">Get-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d214d-101">Get-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="d214d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d214d-102">SYNOPSIS</span></span>
<span data-ttu-id="d214d-103">Контейнеры для учетной записи edge Storage на устройстве.</span><span class="sxs-lookup"><span data-stu-id="d214d-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="d214d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d214d-104">SYNTAX</span></span>

### <span data-ttu-id="d214d-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d214d-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d214d-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d214d-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d214d-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d214d-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d214d-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d214d-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSStackEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="d214d-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d214d-109">DESCRIPTION</span></span>
<span data-ttu-id="d214d-110">Для учетной записи Edge на устройстве Stack Edge можно получить контейнер хранилища для учетной записи **Get-AzStackEdgeStorageContainer.**</span><span class="sxs-lookup"><span data-stu-id="d214d-110">The **Get-AzStackEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="d214d-111">Вы можете указать имя в качестве параметра в cmdlet для получения сведений о конкретном контейнере хранилища.</span><span class="sxs-lookup"><span data-stu-id="d214d-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="d214d-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d214d-112">EXAMPLES</span></span>

### <span data-ttu-id="d214d-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d214d-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="d214d-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d214d-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="d214d-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d214d-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzStackEdgeStorageAccount | Get-AzStackEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="d214d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d214d-116">PARAMETERS</span></span>

### <span data-ttu-id="d214d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d214d-117">-DefaultProfile</span></span>
<span data-ttu-id="d214d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d214d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d214d-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d214d-119">-DeviceName</span></span>
<span data-ttu-id="d214d-120">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="d214d-120">Device Name</span></span>

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

### <span data-ttu-id="d214d-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d214d-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="d214d-122">Укайм существующее имя EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d214d-122">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="d214d-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="d214d-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="d214d-124">Предоставление существующего объекта EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d214d-124">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d214d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d214d-125">-Name</span></span>
<span data-ttu-id="d214d-126">Имя edgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d214d-126">Name of the EdgeStorageContainer</span></span>

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

### <span data-ttu-id="d214d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d214d-127">-ResourceGroupName</span></span>
<span data-ttu-id="d214d-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d214d-128">Resource Group Name</span></span>

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

### <span data-ttu-id="d214d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d214d-129">-ResourceId</span></span>
<span data-ttu-id="d214d-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d214d-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="d214d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d214d-131">CommonParameters</span></span>
<span data-ttu-id="d214d-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d214d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d214d-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d214d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d214d-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d214d-134">INPUTS</span></span>

### <span data-ttu-id="d214d-135">System.String</span><span class="sxs-lookup"><span data-stu-id="d214d-135">System.String</span></span>

### <span data-ttu-id="d214d-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d214d-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="d214d-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d214d-137">OUTPUTS</span></span>

### <span data-ttu-id="d214d-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d214d-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="d214d-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d214d-139">NOTES</span></span>

## <span data-ttu-id="d214d-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d214d-140">RELATED LINKS</span></span>
