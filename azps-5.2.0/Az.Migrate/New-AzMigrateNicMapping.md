---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 118e96747d3859a7b9132747052fb3407b7201ae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408948"
---
# <span data-ttu-id="47b43-101">New-AzMigrateNicMapping</span><span class="sxs-lookup"><span data-stu-id="47b43-101">New-AzMigrateNicMapping</span></span>

## <span data-ttu-id="47b43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47b43-102">SYNOPSIS</span></span>
<span data-ttu-id="47b43-103">Создает объект для обновления свойств NIC сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="47b43-103">Creates an object to update NIC properties of a replicating server.</span></span>

## <span data-ttu-id="47b43-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="47b43-104">SYNTAX</span></span>

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## <span data-ttu-id="47b43-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47b43-105">DESCRIPTION</span></span>
<span data-ttu-id="47b43-106">С New-AzMigrateNicMapping создается сопоставление источника NIC, подключенного к серверу.</span><span class="sxs-lookup"><span data-stu-id="47b43-106">The New-AzMigrateNicMapping cmdlet creates a mapping of the source NIC attached to the server to be migrated.</span></span>
<span data-ttu-id="47b43-107">Этот объект предоставляется в качестве входного Set-AzMigrateServerReplication для обновления NIC и его свойств для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="47b43-107">This object is provided as an input to the Set-AzMigrateServerReplication cmdlet to update the NIC and its properties for a replicating server.</span></span>

## <span data-ttu-id="47b43-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="47b43-108">EXAMPLES</span></span>

### <span data-ttu-id="47b43-109">Пример 1. Создание объекта NIC</span><span class="sxs-lookup"><span data-stu-id="47b43-109">Example 1: Create a NIC object</span></span>
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

<span data-ttu-id="47b43-110">Создает объект обновления NIC.</span><span class="sxs-lookup"><span data-stu-id="47b43-110">Creates a NIC update object.</span></span>

## <span data-ttu-id="47b43-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47b43-111">PARAMETERS</span></span>

### <span data-ttu-id="47b43-112">-NicID</span><span class="sxs-lookup"><span data-stu-id="47b43-112">-NicID</span></span>
<span data-ttu-id="47b43-113">Определяет ID NIC, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="47b43-113">Specifies the ID of the NIC to be updated.</span></span>

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

### <span data-ttu-id="47b43-114">-TargetNicIP</span><span class="sxs-lookup"><span data-stu-id="47b43-114">-TargetNicIP</span></span>
<span data-ttu-id="47b43-115">IP-адрес в подсети назначения, который будет использоваться для NIC.</span><span class="sxs-lookup"><span data-stu-id="47b43-115">Specifies the IP within the destination subnet to be used for the NIC.</span></span>

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

### <span data-ttu-id="47b43-116">-TargetNicSelectionType</span><span class="sxs-lookup"><span data-stu-id="47b43-116">-TargetNicSelectionType</span></span>
<span data-ttu-id="47b43-117">Указывает, будет ли NIC обновляться как основной, дополнительный, так и не перенесенный.</span><span class="sxs-lookup"><span data-stu-id="47b43-117">Specifies whether the NIC to be updated will be the primary, secondary or not migrated.</span></span>

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

### <span data-ttu-id="47b43-118">-TargetNicSubnet</span><span class="sxs-lookup"><span data-stu-id="47b43-118">-TargetNicSubnet</span></span>
<span data-ttu-id="47b43-119">Имя подсети для NIC в сети назначения, в которую требуется перенести сервер.</span><span class="sxs-lookup"><span data-stu-id="47b43-119">Specifies the Subnet name for the NIC in the destination Virtual Network to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="47b43-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b43-120">CommonParameters</span></span>
<span data-ttu-id="47b43-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47b43-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b43-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47b43-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b43-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47b43-123">INPUTS</span></span>

## <span data-ttu-id="47b43-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="47b43-124">OUTPUTS</span></span>

### <span data-ttu-id="47b43-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span><span class="sxs-lookup"><span data-stu-id="47b43-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span></span>

## <span data-ttu-id="47b43-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="47b43-126">NOTES</span></span>

<span data-ttu-id="47b43-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="47b43-127">ALIASES</span></span>

## <span data-ttu-id="47b43-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47b43-128">RELATED LINKS</span></span>

