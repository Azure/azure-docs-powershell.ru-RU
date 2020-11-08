---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 8230056069668765d3d27a9dd54538a310edf383
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250069"
---
# <span data-ttu-id="81d97-101">Get-AzMigrateReplicationFabric</span><span class="sxs-lookup"><span data-stu-id="81d97-101">Get-AzMigrateReplicationFabric</span></span>

## <span data-ttu-id="81d97-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="81d97-102">SYNOPSIS</span></span>
<span data-ttu-id="81d97-103">Получает сведения о структуре восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="81d97-103">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="81d97-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="81d97-104">SYNTAX</span></span>

### <span data-ttu-id="81d97-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="81d97-105">List (Default)</span></span>
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="81d97-106">Получить</span><span class="sxs-lookup"><span data-stu-id="81d97-106">Get</span></span>
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="81d97-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81d97-107">DESCRIPTION</span></span>
<span data-ttu-id="81d97-108">Получает сведения о структуре восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="81d97-108">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="81d97-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="81d97-109">EXAMPLES</span></span>

### <span data-ttu-id="81d97-110">Пример 1: получение всех структур по группе ресурсов и имени хранилища</span><span class="sxs-lookup"><span data-stu-id="81d97-110">Example 1: Get all fabrics by resource group and vault name</span></span>
```powershell
PS C:\> PS Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="81d97-111">Получение всех структур в группе ресурсов и в хранилище</span><span class="sxs-lookup"><span data-stu-id="81d97-111">Get all fabrics in resource group and vault</span></span>

### <span data-ttu-id="81d97-112">Пример 2: получение структуры по группе ресурсов, имени хранилища и имени структуры</span><span class="sxs-lookup"><span data-stu-id="81d97-112">Example 2: Get fabric by resource group, vault name and fabric name</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="81d97-113">Получить определенную структуру</span><span class="sxs-lookup"><span data-stu-id="81d97-113">Get a specific fabric</span></span>

## <span data-ttu-id="81d97-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="81d97-114">PARAMETERS</span></span>

### <span data-ttu-id="81d97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d97-115">-DefaultProfile</span></span>
<span data-ttu-id="81d97-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="81d97-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d97-117">-FabricName</span><span class="sxs-lookup"><span data-stu-id="81d97-117">-FabricName</span></span>
<span data-ttu-id="81d97-118">Имя структуры.</span><span class="sxs-lookup"><span data-stu-id="81d97-118">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d97-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81d97-119">-ResourceGroupName</span></span>
<span data-ttu-id="81d97-120">Имя группы ресурсов, в которой находится хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="81d97-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="81d97-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="81d97-121">-ResourceName</span></span>
<span data-ttu-id="81d97-122">Имя хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="81d97-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="81d97-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="81d97-123">-SubscriptionId</span></span>
<span data-ttu-id="81d97-124">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="81d97-124">The subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d97-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d97-125">CommonParameters</span></span>
<span data-ttu-id="81d97-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="81d97-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d97-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81d97-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d97-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="81d97-128">INPUTS</span></span>

## <span data-ttu-id="81d97-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="81d97-129">OUTPUTS</span></span>

### <span data-ttu-id="81d97-130">Microsoft. Azure. PowerShell. командлеты. remigrate. Models. Api20180110. IFabric</span><span class="sxs-lookup"><span data-stu-id="81d97-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span></span>

## <span data-ttu-id="81d97-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="81d97-131">NOTES</span></span>

<span data-ttu-id="81d97-132">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="81d97-132">ALIASES</span></span>

## <span data-ttu-id="81d97-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81d97-133">RELATED LINKS</span></span>

