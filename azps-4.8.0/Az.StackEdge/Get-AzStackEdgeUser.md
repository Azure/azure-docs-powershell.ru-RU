---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
ms.openlocfilehash: 3a9945d94b1aec3e82d4d79d09df0bacb3b3a11d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235746"
---
# <span data-ttu-id="9622e-101">Get-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="9622e-101">Get-AzStackEdgeUser</span></span>

## <span data-ttu-id="9622e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9622e-102">SYNOPSIS</span></span>
<span data-ttu-id="9622e-103">Возвращает пользователей, настроенных для устройства.</span><span class="sxs-lookup"><span data-stu-id="9622e-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="9622e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9622e-104">SYNTAX</span></span>

### <span data-ttu-id="9622e-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9622e-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9622e-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9622e-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9622e-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9622e-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9622e-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9622e-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="9622e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9622e-109">DESCRIPTION</span></span>
<span data-ttu-id="9622e-110">Командлет **Get-AzStackEdgeUser** содержит список пользователей, настроенных для пограничного устройства в стопке.</span><span class="sxs-lookup"><span data-stu-id="9622e-110">The **Get-AzStackEdgeUser** cmdlet lists the users configured for a Stack Edge device.</span></span> <span data-ttu-id="9622e-111">Вы можете упомянуть имя в параметрах, чтобы получить сведения о конкретном пользователе.</span><span class="sxs-lookup"><span data-stu-id="9622e-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="9622e-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9622e-112">EXAMPLES</span></span>

### <span data-ttu-id="9622e-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9622e-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="9622e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9622e-114">PARAMETERS</span></span>

### <span data-ttu-id="9622e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9622e-115">-DefaultProfile</span></span>
<span data-ttu-id="9622e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9622e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9622e-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="9622e-117">-DeviceName</span></span>
<span data-ttu-id="9622e-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="9622e-118">Device Name</span></span>

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

### <span data-ttu-id="9622e-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="9622e-119">-DeviceObject</span></span>
<span data-ttu-id="9622e-120">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="9622e-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="9622e-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9622e-121">-Name</span></span>
<span data-ttu-id="9622e-122">Действительно</span><span class="sxs-lookup"><span data-stu-id="9622e-122">Username</span></span>

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

### <span data-ttu-id="9622e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9622e-123">-ResourceGroupName</span></span>
<span data-ttu-id="9622e-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9622e-124">Resource Group Name</span></span>

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

### <span data-ttu-id="9622e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9622e-125">-ResourceId</span></span>
<span data-ttu-id="9622e-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9622e-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="9622e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9622e-127">CommonParameters</span></span>
<span data-ttu-id="9622e-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9622e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9622e-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9622e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9622e-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9622e-130">INPUTS</span></span>

### <span data-ttu-id="9622e-131">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="9622e-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="9622e-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9622e-132">OUTPUTS</span></span>

### <span data-ttu-id="9622e-133">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="9622e-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="9622e-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="9622e-134">NOTES</span></span>

## <span data-ttu-id="9622e-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9622e-135">RELATED LINKS</span></span>
