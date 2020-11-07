---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
ms.openlocfilehash: 0ab290934a956282a16d9e2321b2c5ed948f33af
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911285"
---
# <span data-ttu-id="af7b5-101">Get-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="af7b5-101">Get-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="af7b5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af7b5-102">SYNOPSIS</span></span>
<span data-ttu-id="af7b5-103">Возвращает пользователей, настроенных для устройства.</span><span class="sxs-lookup"><span data-stu-id="af7b5-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="af7b5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af7b5-104">SYNTAX</span></span>

### <span data-ttu-id="af7b5-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="af7b5-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af7b5-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="af7b5-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af7b5-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="af7b5-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af7b5-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af7b5-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="af7b5-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af7b5-109">DESCRIPTION</span></span>
<span data-ttu-id="af7b5-110">Командлет **Get-AzDataBoxEdgeUser** содержит список пользователей, настроенных на пограничном устройстве для поля данных.</span><span class="sxs-lookup"><span data-stu-id="af7b5-110">The **Get-AzDataBoxEdgeUser** cmdlet lists the users configured for a Data Box Edge device.</span></span> <span data-ttu-id="af7b5-111">Вы можете упомянуть имя в параметрах, чтобы получить сведения о конкретном пользователе.</span><span class="sxs-lookup"><span data-stu-id="af7b5-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="af7b5-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af7b5-112">EXAMPLES</span></span>

### <span data-ttu-id="af7b5-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="af7b5-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="af7b5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af7b5-114">PARAMETERS</span></span>

### <span data-ttu-id="af7b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af7b5-115">-DefaultProfile</span></span>
<span data-ttu-id="af7b5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af7b5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af7b5-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="af7b5-117">-DeviceName</span></span>
<span data-ttu-id="af7b5-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="af7b5-118">Device Name</span></span>

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

### <span data-ttu-id="af7b5-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="af7b5-119">-DeviceObject</span></span>
<span data-ttu-id="af7b5-120">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="af7b5-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="af7b5-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="af7b5-121">-Name</span></span>
<span data-ttu-id="af7b5-122">Действительно</span><span class="sxs-lookup"><span data-stu-id="af7b5-122">Username</span></span>

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

### <span data-ttu-id="af7b5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af7b5-123">-ResourceGroupName</span></span>
<span data-ttu-id="af7b5-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="af7b5-124">Resource Group Name</span></span>

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

### <span data-ttu-id="af7b5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af7b5-125">-ResourceId</span></span>
<span data-ttu-id="af7b5-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="af7b5-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="af7b5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af7b5-127">CommonParameters</span></span>
<span data-ttu-id="af7b5-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af7b5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af7b5-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af7b5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af7b5-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af7b5-130">INPUTS</span></span>

### <span data-ttu-id="af7b5-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="af7b5-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="af7b5-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af7b5-132">OUTPUTS</span></span>

### <span data-ttu-id="af7b5-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="af7b5-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="af7b5-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="af7b5-134">NOTES</span></span>

## <span data-ttu-id="af7b5-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af7b5-135">RELATED LINKS</span></span>
