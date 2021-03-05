---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeDevice.md
ms.openlocfilehash: dbc5e0bf327383adafa980d3475d196173fa0fdb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011448"
---
# <span data-ttu-id="07808-101">Get-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="07808-101">Get-AzStackEdgeDevice</span></span>

## <span data-ttu-id="07808-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07808-102">SYNOPSIS</span></span>
<span data-ttu-id="07808-103">Возвращает сведения о доступных устройствах Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="07808-103">Gets the information on available Stack Edge devices.</span></span>

## <span data-ttu-id="07808-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="07808-104">SYNTAX</span></span>

### <span data-ttu-id="07808-105">ListByParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07808-105">ListByParameterSet (Default)</span></span>
```
Get-AzStackEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="07808-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07808-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeDevice -ResourceId <String> [-ExtendedInfo] [-NetworkSetting] [-Alert] [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07808-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="07808-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo] [-NetworkSetting] [-Alert]
 [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07808-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07808-108">DESCRIPTION</span></span>
<span data-ttu-id="07808-109">Чтобы получить сведения о доступных устройствах Stack Edge, можно получить сведения **о cmdlet Get-AzStackEdgeDevice.**</span><span class="sxs-lookup"><span data-stu-id="07808-109">The **Get-AzStackEdgeDevice** cmdlet gets the information about the available Stack Edge Devices.</span></span> <span data-ttu-id="07808-110">Вы можете указать имя устройства вместе с именем группы ресурсов, чтобы получить сведения о конкретном устройстве.</span><span class="sxs-lookup"><span data-stu-id="07808-110">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="07808-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="07808-111">EXAMPLES</span></span>

### <span data-ttu-id="07808-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="07808-112">Example 1</span></span>
```powershell
PS C:\>Get-AzStackEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="07808-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="07808-113">Example 2</span></span>
```powershell
PS C:\>$device = Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName1 -DeviceName deviceNameOne -Alert -UpdateSummary -NetworkSetting -ExtendedInfo

PS C:\>$device.Alert

Title                            Severity AppearedDateTime      Recommendation
-----                            -------- ----------------      --------------
Lost heartbeat from your device. Critical 02-Jan-20 10:35:20 AM If your device is offline, then the device is not able to communicate with the Azure service. This could be due to one of the following reasons: <br/> &nbs�


PS C:\>$device.NetworkSetting

State    IPv4         IPv6                                 Subnet        Default Gateway Physical address DNS Servers
-----    ----         ----                                 ------        --------------- ---------------- -----------
Disabled 10.150.76.82 2404:f801:4800:1e:8168:dca6:b3b9:d70 255.255.252.0 10.150.76.1     00155D4E262B     10.50.50.50,10.50.10.50

PS C:\>$device.UpdateSummary

DeviceName        Current Version Friendly name      Last Software Scan Last Software Update Pending Updates Pending Update Titles
----------        --------------- -------------      ------------------ -------------------- --------------- ---------------------
deviceNameOne     2.0.998.537     Data Box Edge Mock                                         0

PS C:\>$device.ExtendedInfo

ResourceGroupName   DeviceName        EncryptedCIK Thumbprint     ResourceKey        EncryptedCIK
-----------------   ----------        -----------------------     -----------        ------------
resourceGroupName1  deviceNameOne     EncryptedCIKThumbpring      411182691329779166 EncryptedCIK
```

## <span data-ttu-id="07808-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07808-114">PARAMETERS</span></span>

### <span data-ttu-id="07808-115">-Оповещение</span><span class="sxs-lookup"><span data-stu-id="07808-115">-Alert</span></span>
<span data-ttu-id="07808-116">Извлечение оповещений на устройстве Edge или шлюза Stack</span><span class="sxs-lookup"><span data-stu-id="07808-116">Fetch the alerts on the Stack edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07808-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07808-117">-DefaultProfile</span></span>
<span data-ttu-id="07808-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07808-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07808-119">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="07808-119">-ExtendedInfo</span></span>
<span data-ttu-id="07808-120">Получает дополнительные сведения для указанного устройства Stack Edge или Stack Gateway.</span><span class="sxs-lookup"><span data-stu-id="07808-120">Gets additional information for the specified Stack Edge/Stack Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07808-121">-Name</span><span class="sxs-lookup"><span data-stu-id="07808-121">-Name</span></span>
<span data-ttu-id="07808-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="07808-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07808-123">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="07808-123">-NetworkSetting</span></span>
<span data-ttu-id="07808-124">Получает параметры сети для указанного устройства Stack Edge или Stack Gateway.</span><span class="sxs-lookup"><span data-stu-id="07808-124">Gets the network settings of the specified Stack Edge/Stack Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07808-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07808-125">-ResourceGroupName</span></span>
<span data-ttu-id="07808-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="07808-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListByParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07808-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07808-127">-ResourceId</span></span>
<span data-ttu-id="07808-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="07808-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="07808-129">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="07808-129">-UpdateSummary</span></span>
<span data-ttu-id="07808-130">Сведения о доступности обновлений на основе последнего сканирования устройства.</span><span class="sxs-lookup"><span data-stu-id="07808-130">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="07808-131">Она также получает сведения обо всех текущих заданиях скачивания и установки на устройстве.</span><span class="sxs-lookup"><span data-stu-id="07808-131">It also gets information about any ongoing download or install jobs on the device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07808-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07808-132">CommonParameters</span></span>
<span data-ttu-id="07808-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07808-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07808-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07808-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07808-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07808-135">INPUTS</span></span>

## <span data-ttu-id="07808-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="07808-136">OUTPUTS</span></span>

## <span data-ttu-id="07808-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="07808-137">NOTES</span></span>

## <span data-ttu-id="07808-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07808-138">RELATED LINKS</span></span>
