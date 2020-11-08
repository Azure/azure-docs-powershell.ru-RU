---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
ms.openlocfilehash: 6a20f81644827c84ee1ce215ad2e87268650caf9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079718"
---
# <span data-ttu-id="c9b49-101">Get-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="c9b49-101">Get-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="c9b49-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9b49-102">SYNOPSIS</span></span>
<span data-ttu-id="c9b49-103">Возвращает доступные общие ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="c9b49-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="c9b49-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9b49-104">SYNTAX</span></span>

### <span data-ttu-id="c9b49-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c9b49-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9b49-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9b49-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9b49-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9b49-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9b49-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9b49-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="c9b49-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9b49-109">DESCRIPTION</span></span>
<span data-ttu-id="c9b49-110">Командлет **Get-AzDataBoxEdgeShare** получает доступные общие ресурсы для пограничного устройства поля данных.</span><span class="sxs-lookup"><span data-stu-id="c9b49-110">The **Get-AzDataBoxEdgeShare** cmdlet gets the available shares for a Data Box Edge device.</span></span> <span data-ttu-id="c9b49-111">Если указано имя, будет получен общий доступ по имени.</span><span class="sxs-lookup"><span data-stu-id="c9b49-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="c9b49-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9b49-112">EXAMPLES</span></span>

### <span data-ttu-id="c9b49-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c9b49-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="c9b49-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9b49-114">PARAMETERS</span></span>

### <span data-ttu-id="c9b49-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9b49-115">-DefaultProfile</span></span>
<span data-ttu-id="c9b49-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c9b49-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9b49-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="c9b49-117">-DeviceName</span></span>
<span data-ttu-id="c9b49-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="c9b49-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b49-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="c9b49-119">-DeviceObject</span></span>
<span data-ttu-id="c9b49-120">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="c9b49-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="c9b49-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c9b49-121">-Name</span></span>
<span data-ttu-id="c9b49-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="c9b49-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b49-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9b49-123">-ResourceGroupName</span></span>
<span data-ttu-id="c9b49-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c9b49-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b49-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9b49-125">-ResourceId</span></span>
<span data-ttu-id="c9b49-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9b49-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b49-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9b49-127">CommonParameters</span></span>
<span data-ttu-id="c9b49-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9b49-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9b49-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9b49-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9b49-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9b49-130">INPUTS</span></span>

### <span data-ttu-id="c9b49-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c9b49-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="c9b49-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9b49-132">OUTPUTS</span></span>

### <span data-ttu-id="c9b49-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="c9b49-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="c9b49-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9b49-134">NOTES</span></span>

## <span data-ttu-id="c9b49-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9b49-135">RELATED LINKS</span></span>
