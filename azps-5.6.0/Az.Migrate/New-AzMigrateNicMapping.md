---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 9ec976cae2afc5070303404616b3615fe54e7b81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982760"
---
# <span data-ttu-id="03f1a-101">New-AzMigrateNicMapping</span><span class="sxs-lookup"><span data-stu-id="03f1a-101">New-AzMigrateNicMapping</span></span>

## <span data-ttu-id="03f1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03f1a-102">SYNOPSIS</span></span>
<span data-ttu-id="03f1a-103">Создает объект для обновления свойств NIC сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="03f1a-103">Creates an object to update NIC properties of a replicating server.</span></span>

## <span data-ttu-id="03f1a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="03f1a-104">SYNTAX</span></span>

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## <span data-ttu-id="03f1a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03f1a-105">DESCRIPTION</span></span>
<span data-ttu-id="03f1a-106">С New-AzMigrateNicMapping создается сопоставление источника NIC, подключенного к серверу.</span><span class="sxs-lookup"><span data-stu-id="03f1a-106">The New-AzMigrateNicMapping cmdlet creates a mapping of the source NIC attached to the server to be migrated.</span></span>
<span data-ttu-id="03f1a-107">Этот объект предоставляется в качестве входного Set-AzMigrateServerReplication NIC и его свойств для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="03f1a-107">This object is provided as an input to the Set-AzMigrateServerReplication cmdlet to update the NIC and its properties for a replicating server.</span></span>

## <span data-ttu-id="03f1a-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="03f1a-108">EXAMPLES</span></span>

### <span data-ttu-id="03f1a-109">Пример 1. Создание объекта NIC</span><span class="sxs-lookup"><span data-stu-id="03f1a-109">Example 1: Create a NIC object</span></span>
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

<span data-ttu-id="03f1a-110">Создает объект обновления NIC.</span><span class="sxs-lookup"><span data-stu-id="03f1a-110">Creates a NIC update object.</span></span>

## <span data-ttu-id="03f1a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03f1a-111">PARAMETERS</span></span>

### <span data-ttu-id="03f1a-112">-NicID</span><span class="sxs-lookup"><span data-stu-id="03f1a-112">-NicID</span></span>
<span data-ttu-id="03f1a-113">Определяет ID NIC, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="03f1a-113">Specifies the ID of the NIC to be updated.</span></span>

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

### <span data-ttu-id="03f1a-114">-TargetNicIP</span><span class="sxs-lookup"><span data-stu-id="03f1a-114">-TargetNicIP</span></span>
<span data-ttu-id="03f1a-115">IP-адрес в подсети назначения, который будет использоваться для NIC.</span><span class="sxs-lookup"><span data-stu-id="03f1a-115">Specifies the IP within the destination subnet to be used for the NIC.</span></span>

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

### <span data-ttu-id="03f1a-116">-TargetNicSelectionType</span><span class="sxs-lookup"><span data-stu-id="03f1a-116">-TargetNicSelectionType</span></span>
<span data-ttu-id="03f1a-117">Указывает, является ли обновляемая NIC основной, дополнительной или не перенесенной.</span><span class="sxs-lookup"><span data-stu-id="03f1a-117">Specifies whether the NIC to be updated will be the primary, secondary or not migrated.</span></span>

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

### <span data-ttu-id="03f1a-118">-TargetNicSubnet</span><span class="sxs-lookup"><span data-stu-id="03f1a-118">-TargetNicSubnet</span></span>
<span data-ttu-id="03f1a-119">Имя подсети для NIC в сети назначения, в которую необходимо перенести сервер.</span><span class="sxs-lookup"><span data-stu-id="03f1a-119">Specifies the Subnet name for the NIC in the destination Virtual Network to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="03f1a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03f1a-120">CommonParameters</span></span>
<span data-ttu-id="03f1a-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03f1a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03f1a-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03f1a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03f1a-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03f1a-123">INPUTS</span></span>

## <span data-ttu-id="03f1a-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="03f1a-124">OUTPUTS</span></span>

### <span data-ttu-id="03f1a-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span><span class="sxs-lookup"><span data-stu-id="03f1a-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span></span>

## <span data-ttu-id="03f1a-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="03f1a-126">NOTES</span></span>

<span data-ttu-id="03f1a-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="03f1a-127">ALIASES</span></span>

## <span data-ttu-id="03f1a-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03f1a-128">RELATED LINKS</span></span>

