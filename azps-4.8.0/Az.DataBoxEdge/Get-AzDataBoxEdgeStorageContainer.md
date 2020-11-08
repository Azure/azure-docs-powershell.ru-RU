---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 3f7ebc42efc2ad5ba73079fd2774614b941f432b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236826"
---
# <span data-ttu-id="6d9bb-101">Get-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6d9bb-101">Get-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="6d9bb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d9bb-102">SYNOPSIS</span></span>
<span data-ttu-id="6d9bb-103">Получает контейнеры для учетной записи хранилища EDGE на устройстве.</span><span class="sxs-lookup"><span data-stu-id="6d9bb-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="6d9bb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d9bb-104">SYNTAX</span></span>

### <span data-ttu-id="6d9bb-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6d9bb-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d9bb-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d9bb-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d9bb-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d9bb-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d9bb-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d9bb-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSDataBoxEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="6d9bb-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d9bb-109">DESCRIPTION</span></span>
<span data-ttu-id="6d9bb-110">Командлет **Get-AzDataBoxEdgeStorageContainer** получает контейнер хранилища для учетной записи пограничного хранилища на пограничном устройстве поля данных.</span><span class="sxs-lookup"><span data-stu-id="6d9bb-110">The **Get-AzDataBoxEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="6d9bb-111">Вы можете указать имя в качестве параметра в командлете, чтобы получить сведения об определенном контейнере хранилища.</span><span class="sxs-lookup"><span data-stu-id="6d9bb-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="6d9bb-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d9bb-112">EXAMPLES</span></span>

### <span data-ttu-id="6d9bb-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6d9bb-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="6d9bb-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6d9bb-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="6d9bb-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6d9bb-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount | Get-AzDataBoxEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="6d9bb-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d9bb-116">PARAMETERS</span></span>

### <span data-ttu-id="6d9bb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d9bb-117">-DefaultProfile</span></span>
<span data-ttu-id="6d9bb-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d9bb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d9bb-119">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="6d9bb-119">-DeviceName</span></span>
<span data-ttu-id="6d9bb-120">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="6d9bb-120">Device Name</span></span>

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

### <span data-ttu-id="6d9bb-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6d9bb-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="6d9bb-122">Укажите имя существующего EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d9bb-122">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="6d9bb-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="6d9bb-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="6d9bb-124">Предоставить существующий объект EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d9bb-124">Provide existing EdgeStorageAccount Object</span></span>

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

### <span data-ttu-id="6d9bb-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6d9bb-125">-Name</span></span>
<span data-ttu-id="6d9bb-126">Имя EdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6d9bb-126">Name of the EdgeStorageContainer</span></span>

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

### <span data-ttu-id="6d9bb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d9bb-127">-ResourceGroupName</span></span>
<span data-ttu-id="6d9bb-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6d9bb-128">Resource Group Name</span></span>

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

### <span data-ttu-id="6d9bb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d9bb-129">-ResourceId</span></span>
<span data-ttu-id="6d9bb-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d9bb-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="6d9bb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d9bb-131">CommonParameters</span></span>
<span data-ttu-id="6d9bb-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d9bb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d9bb-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d9bb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d9bb-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d9bb-134">INPUTS</span></span>

### <span data-ttu-id="6d9bb-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6d9bb-135">System.String</span></span>

### <span data-ttu-id="6d9bb-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d9bb-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="6d9bb-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d9bb-137">OUTPUTS</span></span>

### <span data-ttu-id="6d9bb-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6d9bb-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="6d9bb-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d9bb-139">NOTES</span></span>

## <span data-ttu-id="6d9bb-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d9bb-140">RELATED LINKS</span></span>
