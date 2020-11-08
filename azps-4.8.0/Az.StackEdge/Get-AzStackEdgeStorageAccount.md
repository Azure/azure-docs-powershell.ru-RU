---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 59d01af85279414503b765aea7f326a8670ec1c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235266"
---
# <span data-ttu-id="8bf50-101">Get-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8bf50-101">Get-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="8bf50-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8bf50-102">SYNOPSIS</span></span>
<span data-ttu-id="8bf50-103">Возвращает учетные записи хранилища EDGE на устройстве.</span><span class="sxs-lookup"><span data-stu-id="8bf50-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="8bf50-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8bf50-104">SYNTAX</span></span>

### <span data-ttu-id="8bf50-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8bf50-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bf50-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bf50-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8bf50-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bf50-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bf50-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bf50-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="8bf50-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bf50-109">DESCRIPTION</span></span>
<span data-ttu-id="8bf50-110">Командлет **Get-AzStackEdgeStorageAccount** получает учетные записи хранилища EDGE, доступные на пограничном устройстве стека.</span><span class="sxs-lookup"><span data-stu-id="8bf50-110">The **Get-AzStackEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Stack Edge device.</span></span> <span data-ttu-id="8bf50-111">Вы можете указать имя как параметр в командлете, чтобы получить сведения о конкретной учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="8bf50-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="8bf50-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8bf50-112">EXAMPLES</span></span>

### <span data-ttu-id="8bf50-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8bf50-113">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="8bf50-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8bf50-114">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="8bf50-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8bf50-115">Example 3</span></span>
```powershell
PS C:\> Get-AzStackEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzStackEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="8bf50-116">Пример 4</span><span class="sxs-lookup"><span data-stu-id="8bf50-116">Example 4</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="8bf50-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8bf50-117">PARAMETERS</span></span>

### <span data-ttu-id="8bf50-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bf50-118">-DefaultProfile</span></span>
<span data-ttu-id="8bf50-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8bf50-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bf50-120">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="8bf50-120">-DeviceName</span></span>
<span data-ttu-id="8bf50-121">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="8bf50-121">Device Name</span></span>

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

### <span data-ttu-id="8bf50-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="8bf50-122">-DeviceObject</span></span>
<span data-ttu-id="8bf50-123">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="8bf50-123">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="8bf50-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8bf50-124">-Name</span></span>
<span data-ttu-id="8bf50-125">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="8bf50-125">Resource Name</span></span>

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

### <span data-ttu-id="8bf50-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bf50-126">-ResourceGroupName</span></span>
<span data-ttu-id="8bf50-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8bf50-127">Resource Group Name</span></span>

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

### <span data-ttu-id="8bf50-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bf50-128">-ResourceId</span></span>
<span data-ttu-id="8bf50-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bf50-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="8bf50-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bf50-130">CommonParameters</span></span>
<span data-ttu-id="8bf50-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8bf50-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bf50-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8bf50-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bf50-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8bf50-133">INPUTS</span></span>

### <span data-ttu-id="8bf50-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8bf50-134">System.String</span></span>

### <span data-ttu-id="8bf50-135">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="8bf50-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="8bf50-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bf50-136">OUTPUTS</span></span>

### <span data-ttu-id="8bf50-137">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8bf50-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="8bf50-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="8bf50-138">NOTES</span></span>

## <span data-ttu-id="8bf50-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8bf50-139">RELATED LINKS</span></span>
