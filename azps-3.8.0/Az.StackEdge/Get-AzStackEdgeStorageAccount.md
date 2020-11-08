---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 59d01af85279414503b765aea7f326a8670ec1c2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065528"
---
# <span data-ttu-id="87ea3-101">Get-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="87ea3-101">Get-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="87ea3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87ea3-102">SYNOPSIS</span></span>
<span data-ttu-id="87ea3-103">Возвращает учетные записи хранилища EDGE на устройстве.</span><span class="sxs-lookup"><span data-stu-id="87ea3-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="87ea3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87ea3-104">SYNTAX</span></span>

### <span data-ttu-id="87ea3-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="87ea3-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87ea3-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="87ea3-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87ea3-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="87ea3-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87ea3-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87ea3-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="87ea3-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87ea3-109">DESCRIPTION</span></span>
<span data-ttu-id="87ea3-110">Командлет **Get-AzStackEdgeStorageAccount** получает учетные записи хранилища EDGE, доступные на пограничном устройстве стека.</span><span class="sxs-lookup"><span data-stu-id="87ea3-110">The **Get-AzStackEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Stack Edge device.</span></span> <span data-ttu-id="87ea3-111">Вы можете указать имя как параметр в командлете, чтобы получить сведения о конкретной учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="87ea3-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="87ea3-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87ea3-112">EXAMPLES</span></span>

### <span data-ttu-id="87ea3-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="87ea3-113">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="87ea3-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="87ea3-114">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="87ea3-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="87ea3-115">Example 3</span></span>
```powershell
PS C:\> Get-AzStackEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzStackEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="87ea3-116">Пример 4</span><span class="sxs-lookup"><span data-stu-id="87ea3-116">Example 4</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="87ea3-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87ea3-117">PARAMETERS</span></span>

### <span data-ttu-id="87ea3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87ea3-118">-DefaultProfile</span></span>
<span data-ttu-id="87ea3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87ea3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87ea3-120">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="87ea3-120">-DeviceName</span></span>
<span data-ttu-id="87ea3-121">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="87ea3-121">Device Name</span></span>

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

### <span data-ttu-id="87ea3-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="87ea3-122">-DeviceObject</span></span>
<span data-ttu-id="87ea3-123">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="87ea3-123">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="87ea3-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="87ea3-124">-Name</span></span>
<span data-ttu-id="87ea3-125">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="87ea3-125">Resource Name</span></span>

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

### <span data-ttu-id="87ea3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87ea3-126">-ResourceGroupName</span></span>
<span data-ttu-id="87ea3-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="87ea3-127">Resource Group Name</span></span>

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

### <span data-ttu-id="87ea3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87ea3-128">-ResourceId</span></span>
<span data-ttu-id="87ea3-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="87ea3-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="87ea3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87ea3-130">CommonParameters</span></span>
<span data-ttu-id="87ea3-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87ea3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87ea3-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87ea3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87ea3-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87ea3-133">INPUTS</span></span>

### <span data-ttu-id="87ea3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="87ea3-134">System.String</span></span>

### <span data-ttu-id="87ea3-135">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="87ea3-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="87ea3-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87ea3-136">OUTPUTS</span></span>

### <span data-ttu-id="87ea3-137">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="87ea3-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="87ea3-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="87ea3-138">NOTES</span></span>

## <span data-ttu-id="87ea3-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87ea3-139">RELATED LINKS</span></span>
