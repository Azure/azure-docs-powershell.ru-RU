---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 7b797b4088cab20ee1933ce88a2462288f04653e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314342"
---
# <span data-ttu-id="8d88a-101">Get-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d88a-101">Get-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="8d88a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d88a-102">SYNOPSIS</span></span>
<span data-ttu-id="8d88a-103">Возвращает учетные записи хранилища EDGE на устройстве.</span><span class="sxs-lookup"><span data-stu-id="8d88a-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="8d88a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d88a-104">SYNTAX</span></span>

### <span data-ttu-id="8d88a-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8d88a-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d88a-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d88a-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d88a-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d88a-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d88a-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d88a-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="8d88a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d88a-109">DESCRIPTION</span></span>
<span data-ttu-id="8d88a-110">Командлет **Get-AzDataBoxEdgeStorageAccount** получает учетные записи хранилища EDGE, доступные на пограничном устройстве поля данных.</span><span class="sxs-lookup"><span data-stu-id="8d88a-110">The **Get-AzDataBoxEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Data Box Edge device.</span></span> <span data-ttu-id="8d88a-111">Вы можете указать имя как параметр в командлете, чтобы получить сведения о конкретной учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="8d88a-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="8d88a-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d88a-112">EXAMPLES</span></span>

### <span data-ttu-id="8d88a-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8d88a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="8d88a-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8d88a-114">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="8d88a-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8d88a-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="8d88a-116">Пример 4</span><span class="sxs-lookup"><span data-stu-id="8d88a-116">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="8d88a-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d88a-117">PARAMETERS</span></span>

### <span data-ttu-id="8d88a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d88a-118">-DefaultProfile</span></span>
<span data-ttu-id="8d88a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d88a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d88a-120">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="8d88a-120">-DeviceName</span></span>
<span data-ttu-id="8d88a-121">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="8d88a-121">Device Name</span></span>

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

### <span data-ttu-id="8d88a-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="8d88a-122">-DeviceObject</span></span>
<span data-ttu-id="8d88a-123">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="8d88a-123">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="8d88a-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8d88a-124">-Name</span></span>
<span data-ttu-id="8d88a-125">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="8d88a-125">Resource Name</span></span>

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

### <span data-ttu-id="8d88a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d88a-126">-ResourceGroupName</span></span>
<span data-ttu-id="8d88a-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8d88a-127">Resource Group Name</span></span>

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

### <span data-ttu-id="8d88a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d88a-128">-ResourceId</span></span>
<span data-ttu-id="8d88a-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d88a-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="8d88a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d88a-130">CommonParameters</span></span>
<span data-ttu-id="8d88a-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d88a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d88a-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d88a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d88a-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d88a-133">INPUTS</span></span>

### <span data-ttu-id="8d88a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8d88a-134">System.String</span></span>

### <span data-ttu-id="8d88a-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="8d88a-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="8d88a-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d88a-136">OUTPUTS</span></span>

### <span data-ttu-id="8d88a-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d88a-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="8d88a-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d88a-138">NOTES</span></span>

## <span data-ttu-id="8d88a-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d88a-139">RELATED LINKS</span></span>
