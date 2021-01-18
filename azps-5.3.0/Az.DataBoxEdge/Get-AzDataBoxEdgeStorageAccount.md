---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 7b797b4088cab20ee1933ce88a2462288f04653e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519098"
---
# <span data-ttu-id="e3809-101">Get-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3809-101">Get-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="e3809-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3809-102">SYNOPSIS</span></span>
<span data-ttu-id="e3809-103">Получает учетные записи edge Storage на устройстве.</span><span class="sxs-lookup"><span data-stu-id="e3809-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="e3809-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e3809-104">SYNTAX</span></span>

### <span data-ttu-id="e3809-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e3809-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3809-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3809-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3809-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3809-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3809-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3809-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="e3809-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3809-109">DESCRIPTION</span></span>
<span data-ttu-id="e3809-110">Для учетных записей Edge Storage, доступных на устройстве Edge Data Box, можно получить учетные записи **Get-AzDataBoxEdgeStorageAccount.**</span><span class="sxs-lookup"><span data-stu-id="e3809-110">The **Get-AzDataBoxEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Data Box Edge device.</span></span> <span data-ttu-id="e3809-111">Вы можете указать имя в качестве параметра в cmdlet, чтобы получить сведения об определенной учетной записи edge Storage.</span><span class="sxs-lookup"><span data-stu-id="e3809-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="e3809-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e3809-112">EXAMPLES</span></span>

### <span data-ttu-id="e3809-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e3809-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="e3809-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e3809-114">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="e3809-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e3809-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="e3809-116">Пример 4</span><span class="sxs-lookup"><span data-stu-id="e3809-116">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="e3809-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3809-117">PARAMETERS</span></span>

### <span data-ttu-id="e3809-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3809-118">-DefaultProfile</span></span>
<span data-ttu-id="e3809-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3809-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3809-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e3809-120">-DeviceName</span></span>
<span data-ttu-id="e3809-121">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="e3809-121">Device Name</span></span>

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

### <span data-ttu-id="e3809-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="e3809-122">-DeviceObject</span></span>
<span data-ttu-id="e3809-123">Предосообщите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="e3809-123">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3809-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e3809-124">-Name</span></span>
<span data-ttu-id="e3809-125">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="e3809-125">Resource Name</span></span>

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

### <span data-ttu-id="e3809-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3809-126">-ResourceGroupName</span></span>
<span data-ttu-id="e3809-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e3809-127">Resource Group Name</span></span>

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

### <span data-ttu-id="e3809-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3809-128">-ResourceId</span></span>
<span data-ttu-id="e3809-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3809-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="e3809-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3809-130">CommonParameters</span></span>
<span data-ttu-id="e3809-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3809-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3809-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3809-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3809-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3809-133">INPUTS</span></span>

### <span data-ttu-id="e3809-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e3809-134">System.String</span></span>

### <span data-ttu-id="e3809-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e3809-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="e3809-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e3809-136">OUTPUTS</span></span>

### <span data-ttu-id="e3809-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3809-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="e3809-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e3809-138">NOTES</span></span>

## <span data-ttu-id="e3809-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3809-139">RELATED LINKS</span></span>
