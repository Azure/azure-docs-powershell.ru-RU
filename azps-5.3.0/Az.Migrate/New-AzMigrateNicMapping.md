---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 118e96747d3859a7b9132747052fb3407b7201ae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425503"
---
# <span data-ttu-id="69f7e-101">New-AzMigrateNicMapping</span><span class="sxs-lookup"><span data-stu-id="69f7e-101">New-AzMigrateNicMapping</span></span>

## <span data-ttu-id="69f7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69f7e-102">SYNOPSIS</span></span>
<span data-ttu-id="69f7e-103">Создает объект для обновления свойств NIC сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="69f7e-103">Creates an object to update NIC properties of a replicating server.</span></span>

## <span data-ttu-id="69f7e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="69f7e-104">SYNTAX</span></span>

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## <span data-ttu-id="69f7e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69f7e-105">DESCRIPTION</span></span>
<span data-ttu-id="69f7e-106">С New-AzMigrateNicMapping создается сопоставление источника NIC, подключенного к серверу.</span><span class="sxs-lookup"><span data-stu-id="69f7e-106">The New-AzMigrateNicMapping cmdlet creates a mapping of the source NIC attached to the server to be migrated.</span></span>
<span data-ttu-id="69f7e-107">Этот объект предоставляется в качестве входного Set-AzMigrateServerReplication NIC и его свойств для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="69f7e-107">This object is provided as an input to the Set-AzMigrateServerReplication cmdlet to update the NIC and its properties for a replicating server.</span></span>

## <span data-ttu-id="69f7e-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="69f7e-108">EXAMPLES</span></span>

### <span data-ttu-id="69f7e-109">Пример 1. Создание объекта NIC</span><span class="sxs-lookup"><span data-stu-id="69f7e-109">Example 1: Create a NIC object</span></span>
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

<span data-ttu-id="69f7e-110">Создает объект обновления NIC.</span><span class="sxs-lookup"><span data-stu-id="69f7e-110">Creates a NIC update object.</span></span>

## <span data-ttu-id="69f7e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69f7e-111">PARAMETERS</span></span>

### <span data-ttu-id="69f7e-112">-NicID</span><span class="sxs-lookup"><span data-stu-id="69f7e-112">-NicID</span></span>
<span data-ttu-id="69f7e-113">Определяет ID NIC, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="69f7e-113">Specifies the ID of the NIC to be updated.</span></span>

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

### <span data-ttu-id="69f7e-114">-TargetNicIP</span><span class="sxs-lookup"><span data-stu-id="69f7e-114">-TargetNicIP</span></span>
<span data-ttu-id="69f7e-115">IP-адрес в подсети назначения, который будет использоваться для NIC.</span><span class="sxs-lookup"><span data-stu-id="69f7e-115">Specifies the IP within the destination subnet to be used for the NIC.</span></span>

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

### <span data-ttu-id="69f7e-116">-TargetNicSelectionType</span><span class="sxs-lookup"><span data-stu-id="69f7e-116">-TargetNicSelectionType</span></span>
<span data-ttu-id="69f7e-117">Указывает, будет ли NIC обновляться как основной, дополнительный, так и не перенесенный.</span><span class="sxs-lookup"><span data-stu-id="69f7e-117">Specifies whether the NIC to be updated will be the primary, secondary or not migrated.</span></span>

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

### <span data-ttu-id="69f7e-118">-TargetNicSubnet</span><span class="sxs-lookup"><span data-stu-id="69f7e-118">-TargetNicSubnet</span></span>
<span data-ttu-id="69f7e-119">Имя подсети для NIC в сети назначения, в которую необходимо перенести сервер.</span><span class="sxs-lookup"><span data-stu-id="69f7e-119">Specifies the Subnet name for the NIC in the destination Virtual Network to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="69f7e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69f7e-120">CommonParameters</span></span>
<span data-ttu-id="69f7e-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69f7e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69f7e-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69f7e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69f7e-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69f7e-123">INPUTS</span></span>

## <span data-ttu-id="69f7e-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="69f7e-124">OUTPUTS</span></span>

### <span data-ttu-id="69f7e-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span><span class="sxs-lookup"><span data-stu-id="69f7e-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span></span>

## <span data-ttu-id="69f7e-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="69f7e-126">NOTES</span></span>

<span data-ttu-id="69f7e-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="69f7e-127">ALIASES</span></span>

## <span data-ttu-id="69f7e-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69f7e-128">RELATED LINKS</span></span>

