---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 118e96747d3859a7b9132747052fb3407b7201ae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248870"
---
# <span data-ttu-id="bebff-101">New-AzMigrateNicMapping</span><span class="sxs-lookup"><span data-stu-id="bebff-101">New-AzMigrateNicMapping</span></span>

## <span data-ttu-id="bebff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bebff-102">SYNOPSIS</span></span>
<span data-ttu-id="bebff-103">Создает объект для обновления свойств сетевого адаптера сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="bebff-103">Creates an object to update NIC properties of a replicating server.</span></span>

## <span data-ttu-id="bebff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bebff-104">SYNTAX</span></span>

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## <span data-ttu-id="bebff-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bebff-105">DESCRIPTION</span></span>
<span data-ttu-id="bebff-106">Командлет New-AzMigrateNicMapping создает сопоставление исходного сетевого адаптера, подключенного к серверу для миграции.</span><span class="sxs-lookup"><span data-stu-id="bebff-106">The New-AzMigrateNicMapping cmdlet creates a mapping of the source NIC attached to the server to be migrated.</span></span>
<span data-ttu-id="bebff-107">Этот объект предоставляется в качестве входных данных для командлета Set-AzMigrateServerReplication, чтобы обновить NIC и его свойства для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="bebff-107">This object is provided as an input to the Set-AzMigrateServerReplication cmdlet to update the NIC and its properties for a replicating server.</span></span>

## <span data-ttu-id="bebff-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bebff-108">EXAMPLES</span></span>

### <span data-ttu-id="bebff-109">Пример 1: создание объекта NIC</span><span class="sxs-lookup"><span data-stu-id="bebff-109">Example 1: Create a NIC object</span></span>
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

<span data-ttu-id="bebff-110">Создание объекта обновления сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="bebff-110">Creates a NIC update object.</span></span>

## <span data-ttu-id="bebff-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bebff-111">PARAMETERS</span></span>

### <span data-ttu-id="bebff-112">-NicID</span><span class="sxs-lookup"><span data-stu-id="bebff-112">-NicID</span></span>
<span data-ttu-id="bebff-113">Указывает ИД сетевого адаптера, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="bebff-113">Specifies the ID of the NIC to be updated.</span></span>

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

### <span data-ttu-id="bebff-114">-TargetNicIP</span><span class="sxs-lookup"><span data-stu-id="bebff-114">-TargetNicIP</span></span>
<span data-ttu-id="bebff-115">Указывает IP-адрес в конечной подсети, который будет использоваться для сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="bebff-115">Specifies the IP within the destination subnet to be used for the NIC.</span></span>

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

### <span data-ttu-id="bebff-116">-TargetNicSelectionType</span><span class="sxs-lookup"><span data-stu-id="bebff-116">-TargetNicSelectionType</span></span>
<span data-ttu-id="bebff-117">Указывает, будет ли обновленная сетевая плата являться первичной, дополнительной или не перенесенной.</span><span class="sxs-lookup"><span data-stu-id="bebff-117">Specifies whether the NIC to be updated will be the primary, secondary or not migrated.</span></span>

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

### <span data-ttu-id="bebff-118">-TargetNicSubnet</span><span class="sxs-lookup"><span data-stu-id="bebff-118">-TargetNicSubnet</span></span>
<span data-ttu-id="bebff-119">Указывает имя подсети для NIC в виртуальной сети назначения, на которую необходимо выполнить миграцию сервера.</span><span class="sxs-lookup"><span data-stu-id="bebff-119">Specifies the Subnet name for the NIC in the destination Virtual Network to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="bebff-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bebff-120">CommonParameters</span></span>
<span data-ttu-id="bebff-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bebff-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bebff-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bebff-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bebff-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bebff-123">INPUTS</span></span>

## <span data-ttu-id="bebff-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bebff-124">OUTPUTS</span></span>

### <span data-ttu-id="bebff-125">Microsoft. Azure. PowerShell. командлеты. remigrate. Models. Api20180110. IVMwareCbtNicInput</span><span class="sxs-lookup"><span data-stu-id="bebff-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span></span>

## <span data-ttu-id="bebff-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="bebff-126">NOTES</span></span>

<span data-ttu-id="bebff-127">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="bebff-127">ALIASES</span></span>

## <span data-ttu-id="bebff-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bebff-128">RELATED LINKS</span></span>

