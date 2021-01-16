---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 0b18183b27f5701036afb74bb85768b48e9492e8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394156"
---
# <span data-ttu-id="cc373-101">Get-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cc373-101">Get-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="cc373-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc373-102">SYNOPSIS</span></span>
<span data-ttu-id="cc373-103">Контейнеры для учетной записи edge Storage на устройстве.</span><span class="sxs-lookup"><span data-stu-id="cc373-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="cc373-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cc373-104">SYNTAX</span></span>

### <span data-ttu-id="cc373-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cc373-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc373-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc373-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc373-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc373-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc373-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc373-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSStackEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="cc373-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc373-109">DESCRIPTION</span></span>
<span data-ttu-id="cc373-110">Для учетной записи Edge на устройстве Stack Edge можно получить контейнер хранилища для учетной записи **Get-AzStackEdgeStorageContainer.**</span><span class="sxs-lookup"><span data-stu-id="cc373-110">The **Get-AzStackEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="cc373-111">Вы можете указать имя в качестве параметра в cmdlet для получения сведений о конкретном контейнере хранилища.</span><span class="sxs-lookup"><span data-stu-id="cc373-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="cc373-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cc373-112">EXAMPLES</span></span>

### <span data-ttu-id="cc373-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cc373-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="cc373-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cc373-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="cc373-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="cc373-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzStackEdgeStorageAccount | Get-AzStackEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="cc373-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc373-116">PARAMETERS</span></span>

### <span data-ttu-id="cc373-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc373-117">-DefaultProfile</span></span>
<span data-ttu-id="cc373-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc373-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc373-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="cc373-119">-DeviceName</span></span>
<span data-ttu-id="cc373-120">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="cc373-120">Device Name</span></span>

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

### <span data-ttu-id="cc373-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cc373-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="cc373-122">Укайм существующее имя EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cc373-122">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="cc373-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="cc373-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="cc373-124">Предоставление существующего объекта EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cc373-124">Provide existing EdgeStorageAccount Object</span></span>

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

### <span data-ttu-id="cc373-125">-Name</span><span class="sxs-lookup"><span data-stu-id="cc373-125">-Name</span></span>
<span data-ttu-id="cc373-126">Имя edgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cc373-126">Name of the EdgeStorageContainer</span></span>

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

### <span data-ttu-id="cc373-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc373-127">-ResourceGroupName</span></span>
<span data-ttu-id="cc373-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cc373-128">Resource Group Name</span></span>

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

### <span data-ttu-id="cc373-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc373-129">-ResourceId</span></span>
<span data-ttu-id="cc373-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc373-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="cc373-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc373-131">CommonParameters</span></span>
<span data-ttu-id="cc373-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc373-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc373-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc373-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc373-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc373-134">INPUTS</span></span>

### <span data-ttu-id="cc373-135">System.String</span><span class="sxs-lookup"><span data-stu-id="cc373-135">System.String</span></span>

### <span data-ttu-id="cc373-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cc373-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="cc373-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cc373-137">OUTPUTS</span></span>

### <span data-ttu-id="cc373-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cc373-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="cc373-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cc373-139">NOTES</span></span>

## <span data-ttu-id="cc373-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc373-140">RELATED LINKS</span></span>
