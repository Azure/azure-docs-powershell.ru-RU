---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
ms.openlocfilehash: 3a9945d94b1aec3e82d4d79d09df0bacb3b3a11d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065522"
---
# <span data-ttu-id="7079b-101">Get-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="7079b-101">Get-AzStackEdgeUser</span></span>

## <span data-ttu-id="7079b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7079b-102">SYNOPSIS</span></span>
<span data-ttu-id="7079b-103">Возвращает пользователей, настроенных для устройства.</span><span class="sxs-lookup"><span data-stu-id="7079b-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="7079b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7079b-104">SYNTAX</span></span>

### <span data-ttu-id="7079b-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7079b-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7079b-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7079b-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7079b-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7079b-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7079b-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7079b-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="7079b-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7079b-109">DESCRIPTION</span></span>
<span data-ttu-id="7079b-110">Командлет **Get-AzStackEdgeUser** содержит список пользователей, настроенных для пограничного устройства в стопке.</span><span class="sxs-lookup"><span data-stu-id="7079b-110">The **Get-AzStackEdgeUser** cmdlet lists the users configured for a Stack Edge device.</span></span> <span data-ttu-id="7079b-111">Вы можете упомянуть имя в параметрах, чтобы получить сведения о конкретном пользователе.</span><span class="sxs-lookup"><span data-stu-id="7079b-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="7079b-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7079b-112">EXAMPLES</span></span>

### <span data-ttu-id="7079b-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7079b-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="7079b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7079b-114">PARAMETERS</span></span>

### <span data-ttu-id="7079b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7079b-115">-DefaultProfile</span></span>
<span data-ttu-id="7079b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7079b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7079b-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="7079b-117">-DeviceName</span></span>
<span data-ttu-id="7079b-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="7079b-118">Device Name</span></span>

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

### <span data-ttu-id="7079b-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="7079b-119">-DeviceObject</span></span>
<span data-ttu-id="7079b-120">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="7079b-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="7079b-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7079b-121">-Name</span></span>
<span data-ttu-id="7079b-122">Действительно</span><span class="sxs-lookup"><span data-stu-id="7079b-122">Username</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: Username

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7079b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7079b-123">-ResourceGroupName</span></span>
<span data-ttu-id="7079b-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7079b-124">Resource Group Name</span></span>

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

### <span data-ttu-id="7079b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7079b-125">-ResourceId</span></span>
<span data-ttu-id="7079b-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7079b-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="7079b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7079b-127">CommonParameters</span></span>
<span data-ttu-id="7079b-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7079b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7079b-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7079b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7079b-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7079b-130">INPUTS</span></span>

### <span data-ttu-id="7079b-131">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="7079b-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="7079b-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7079b-132">OUTPUTS</span></span>

### <span data-ttu-id="7079b-133">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="7079b-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="7079b-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="7079b-134">NOTES</span></span>

## <span data-ttu-id="7079b-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7079b-135">RELATED LINKS</span></span>
