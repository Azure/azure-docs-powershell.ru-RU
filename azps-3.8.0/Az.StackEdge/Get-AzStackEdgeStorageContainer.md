---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 0b18183b27f5701036afb74bb85768b48e9492e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065521"
---
# <span data-ttu-id="bff71-101">Get-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="bff71-101">Get-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="bff71-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bff71-102">SYNOPSIS</span></span>
<span data-ttu-id="bff71-103">Получает контейнеры для учетной записи хранилища EDGE на устройстве.</span><span class="sxs-lookup"><span data-stu-id="bff71-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="bff71-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bff71-104">SYNTAX</span></span>

### <span data-ttu-id="bff71-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bff71-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bff71-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bff71-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bff71-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bff71-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bff71-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bff71-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSStackEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="bff71-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bff71-109">DESCRIPTION</span></span>
<span data-ttu-id="bff71-110">Командлет **Get-AzStackEdgeStorageContainer** получает контейнер хранилища для учетной записи хранилища EDGE на пограничном устройстве стопки.</span><span class="sxs-lookup"><span data-stu-id="bff71-110">The **Get-AzStackEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="bff71-111">Вы можете указать имя в качестве параметра в командлете, чтобы получить сведения об определенном контейнере хранилища.</span><span class="sxs-lookup"><span data-stu-id="bff71-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="bff71-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bff71-112">EXAMPLES</span></span>

### <span data-ttu-id="bff71-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bff71-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="bff71-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bff71-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="bff71-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="bff71-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzStackEdgeStorageAccount | Get-AzStackEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="bff71-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bff71-116">PARAMETERS</span></span>

### <span data-ttu-id="bff71-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff71-117">-DefaultProfile</span></span>
<span data-ttu-id="bff71-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bff71-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bff71-119">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="bff71-119">-DeviceName</span></span>
<span data-ttu-id="bff71-120">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="bff71-120">Device Name</span></span>

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

### <span data-ttu-id="bff71-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bff71-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="bff71-122">Укажите имя существующего EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bff71-122">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="bff71-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="bff71-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="bff71-124">Предоставить существующий объект EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bff71-124">Provide existing EdgeStorageAccount Object</span></span>

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

### <span data-ttu-id="bff71-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bff71-125">-Name</span></span>
<span data-ttu-id="bff71-126">Имя EdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="bff71-126">Name of the EdgeStorageContainer</span></span>

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

### <span data-ttu-id="bff71-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bff71-127">-ResourceGroupName</span></span>
<span data-ttu-id="bff71-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="bff71-128">Resource Group Name</span></span>

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

### <span data-ttu-id="bff71-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bff71-129">-ResourceId</span></span>
<span data-ttu-id="bff71-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="bff71-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="bff71-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff71-131">CommonParameters</span></span>
<span data-ttu-id="bff71-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bff71-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff71-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bff71-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff71-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bff71-134">INPUTS</span></span>

### <span data-ttu-id="bff71-135">System. String</span><span class="sxs-lookup"><span data-stu-id="bff71-135">System.String</span></span>

### <span data-ttu-id="bff71-136">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bff71-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="bff71-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bff71-137">OUTPUTS</span></span>

### <span data-ttu-id="bff71-138">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="bff71-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="bff71-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="bff71-139">NOTES</span></span>

## <span data-ttu-id="bff71-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bff71-140">RELATED LINKS</span></span>
