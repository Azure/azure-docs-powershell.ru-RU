---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 118e96747d3859a7b9132747052fb3407b7201ae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237401"
---
# <span data-ttu-id="e7e38-101">New-AzMigrateNicMapping</span><span class="sxs-lookup"><span data-stu-id="e7e38-101">New-AzMigrateNicMapping</span></span>

## <span data-ttu-id="e7e38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7e38-102">SYNOPSIS</span></span>
<span data-ttu-id="e7e38-103">Создает объект для обновления свойств NIC сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="e7e38-103">Creates an object to update NIC properties of a replicating server.</span></span>

## <span data-ttu-id="e7e38-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e7e38-104">SYNTAX</span></span>

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## <span data-ttu-id="e7e38-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7e38-105">DESCRIPTION</span></span>
<span data-ttu-id="e7e38-106">С New-AzMigrateNicMapping создается сопоставление источника NIC, подключенного к серверу.</span><span class="sxs-lookup"><span data-stu-id="e7e38-106">The New-AzMigrateNicMapping cmdlet creates a mapping of the source NIC attached to the server to be migrated.</span></span>
<span data-ttu-id="e7e38-107">Этот объект предоставляется в качестве входного Set-AzMigrateServerReplication для обновления NIC и его свойств для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="e7e38-107">This object is provided as an input to the Set-AzMigrateServerReplication cmdlet to update the NIC and its properties for a replicating server.</span></span>

## <span data-ttu-id="e7e38-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e7e38-108">EXAMPLES</span></span>

### <span data-ttu-id="e7e38-109">Пример 1. Создание объекта NIC</span><span class="sxs-lookup"><span data-stu-id="e7e38-109">Example 1: Create a NIC object</span></span>
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

<span data-ttu-id="e7e38-110">Создает объект обновления NIC.</span><span class="sxs-lookup"><span data-stu-id="e7e38-110">Creates a NIC update object.</span></span>

## <span data-ttu-id="e7e38-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7e38-111">PARAMETERS</span></span>

### <span data-ttu-id="e7e38-112">-NicID</span><span class="sxs-lookup"><span data-stu-id="e7e38-112">-NicID</span></span>
<span data-ttu-id="e7e38-113">Определяет ID NIC, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="e7e38-113">Specifies the ID of the NIC to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7e38-114">-TargetNicIP</span><span class="sxs-lookup"><span data-stu-id="e7e38-114">-TargetNicIP</span></span>
<span data-ttu-id="e7e38-115">IP-адрес в подсети назначения, который будет использоваться для NIC.</span><span class="sxs-lookup"><span data-stu-id="e7e38-115">Specifies the IP within the destination subnet to be used for the NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7e38-116">-TargetNicSelectionType</span><span class="sxs-lookup"><span data-stu-id="e7e38-116">-TargetNicSelectionType</span></span>
<span data-ttu-id="e7e38-117">Указывает, будет ли NIC обновляться как основной, дополнительный, так и не перенесенный.</span><span class="sxs-lookup"><span data-stu-id="e7e38-117">Specifies whether the NIC to be updated will be the primary, secondary or not migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7e38-118">-TargetNicSubnet</span><span class="sxs-lookup"><span data-stu-id="e7e38-118">-TargetNicSubnet</span></span>
<span data-ttu-id="e7e38-119">Имя подсети для NIC в сети назначения, в которую требуется перенести сервер.</span><span class="sxs-lookup"><span data-stu-id="e7e38-119">Specifies the Subnet name for the NIC in the destination Virtual Network to which the server needs to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7e38-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7e38-120">CommonParameters</span></span>
<span data-ttu-id="e7e38-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7e38-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7e38-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7e38-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7e38-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7e38-123">INPUTS</span></span>

## <span data-ttu-id="e7e38-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e7e38-124">OUTPUTS</span></span>

### <span data-ttu-id="e7e38-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span><span class="sxs-lookup"><span data-stu-id="e7e38-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span></span>

## <span data-ttu-id="e7e38-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e7e38-126">NOTES</span></span>

<span data-ttu-id="e7e38-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e7e38-127">ALIASES</span></span>

## <span data-ttu-id="e7e38-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7e38-128">RELATED LINKS</span></span>

