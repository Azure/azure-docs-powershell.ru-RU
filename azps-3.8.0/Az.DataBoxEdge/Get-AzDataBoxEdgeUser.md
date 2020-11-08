---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
ms.openlocfilehash: cc03472aa71665a8612e17bfce6365a255f929bd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073411"
---
# <span data-ttu-id="34c4f-101">Get-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="34c4f-101">Get-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="34c4f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="34c4f-103">Возвращает пользователей, настроенных для устройства.</span><span class="sxs-lookup"><span data-stu-id="34c4f-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="34c4f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34c4f-104">SYNTAX</span></span>

### <span data-ttu-id="34c4f-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="34c4f-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34c4f-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="34c4f-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34c4f-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="34c4f-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34c4f-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34c4f-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="34c4f-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34c4f-109">DESCRIPTION</span></span>
<span data-ttu-id="34c4f-110">Командлет **Get-AzDataBoxEdgeUser** содержит список пользователей, настроенных на пограничном устройстве для поля данных.</span><span class="sxs-lookup"><span data-stu-id="34c4f-110">The **Get-AzDataBoxEdgeUser** cmdlet lists the users configured for a Data Box Edge device.</span></span> <span data-ttu-id="34c4f-111">Вы можете упомянуть имя в параметрах, чтобы получить сведения о конкретном пользователе.</span><span class="sxs-lookup"><span data-stu-id="34c4f-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="34c4f-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34c4f-112">EXAMPLES</span></span>

### <span data-ttu-id="34c4f-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="34c4f-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="34c4f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34c4f-114">PARAMETERS</span></span>

### <span data-ttu-id="34c4f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34c4f-115">-DefaultProfile</span></span>
<span data-ttu-id="34c4f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34c4f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34c4f-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="34c4f-117">-DeviceName</span></span>
<span data-ttu-id="34c4f-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="34c4f-118">Device Name</span></span>

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

### <span data-ttu-id="34c4f-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="34c4f-119">-DeviceObject</span></span>
<span data-ttu-id="34c4f-120">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="34c4f-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="34c4f-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="34c4f-121">-Name</span></span>
<span data-ttu-id="34c4f-122">Действительно</span><span class="sxs-lookup"><span data-stu-id="34c4f-122">Username</span></span>

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

### <span data-ttu-id="34c4f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34c4f-123">-ResourceGroupName</span></span>
<span data-ttu-id="34c4f-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="34c4f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="34c4f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34c4f-125">-ResourceId</span></span>
<span data-ttu-id="34c4f-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="34c4f-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="34c4f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c4f-127">CommonParameters</span></span>
<span data-ttu-id="34c4f-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34c4f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c4f-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34c4f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c4f-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34c4f-130">INPUTS</span></span>

### <span data-ttu-id="34c4f-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="34c4f-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="34c4f-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34c4f-132">OUTPUTS</span></span>

### <span data-ttu-id="34c4f-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="34c4f-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="34c4f-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="34c4f-134">NOTES</span></span>

## <span data-ttu-id="34c4f-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34c4f-135">RELATED LINKS</span></span>
