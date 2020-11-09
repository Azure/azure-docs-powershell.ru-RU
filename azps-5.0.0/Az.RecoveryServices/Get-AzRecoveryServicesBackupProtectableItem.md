---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: add399ca208cdcd1f1b4395523f8df43875ff451
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248484"
---
# <span data-ttu-id="c2a3f-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c2a3f-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="c2a3f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="c2a3f-103">Эта команда будет получать все защищаемые элементы в определенном контейнере или во всех зарегистрированных контейнерах.</span><span class="sxs-lookup"><span data-stu-id="c2a3f-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="c2a3f-104">Он будет состоять из всех элементов иерархии приложения.</span><span class="sxs-lookup"><span data-stu-id="c2a3f-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="c2a3f-105">Возвращает DBs и их элементы верхнего уровня, такие как экземпляр, AvailabilityGroup и т. д.</span><span class="sxs-lookup"><span data-stu-id="c2a3f-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="c2a3f-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2a3f-106">SYNTAX</span></span>

### <span data-ttu-id="c2a3f-107">NoFilterParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2a3f-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2a3f-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="c2a3f-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2a3f-109">IdParamSet</span><span class="sxs-lookup"><span data-stu-id="c2a3f-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2a3f-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2a3f-110">DESCRIPTION</span></span>
<span data-ttu-id="c2a3f-111">Командлет **Get-AzRecoveryServicesBackupProtectableItem** получает список защищенных элементов в контейнере и состояние защиты элементов.</span><span class="sxs-lookup"><span data-stu-id="c2a3f-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the list of protectable items in a container and the protection status of the items.</span></span>
<span data-ttu-id="c2a3f-112">Контейнер, зарегистрированный в хранилище служб восстановления Azure, может содержать один или несколько элементов, которые можно защитить.</span><span class="sxs-lookup"><span data-stu-id="c2a3f-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="c2a3f-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2a3f-113">EXAMPLES</span></span>

### <span data-ttu-id="c2a3f-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c2a3f-114">Example 1</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType MSSQL -Status Registered
PS C:\> $Item = Get-AzRecoveryServicesProtectableItem -Container $Container -ItemType "SQLDatabase" -VaultId $vault.ID
```

<span data-ttu-id="c2a3f-115">Первая команда получает контейнер типа MSSQL и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="c2a3f-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="c2a3f-116">Вторая команда получает защищаемый элемент резервного копирования в $Container, а затем сохраняет его в переменной $Item.</span><span class="sxs-lookup"><span data-stu-id="c2a3f-116">The second command gets the Backup protectable item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="c2a3f-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2a3f-117">PARAMETERS</span></span>

### <span data-ttu-id="c2a3f-118">-Container</span><span class="sxs-lookup"><span data-stu-id="c2a3f-118">-Container</span></span>
<span data-ttu-id="c2a3f-119">Контейнер, в котором находится элемент</span><span class="sxs-lookup"><span data-stu-id="c2a3f-119">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a3f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2a3f-120">-DefaultProfile</span></span>
<span data-ttu-id="c2a3f-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2a3f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2a3f-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="c2a3f-122">-ItemType</span></span>
<span data-ttu-id="c2a3f-123">Указывает тип защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="c2a3f-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="c2a3f-124">Применимые значения: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span><span class="sxs-lookup"><span data-stu-id="c2a3f-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemType
Parameter Sets: FilterParamSet, IdParamSet
Aliases:
Accepted values: SQLDataBase, SQLInstance, SQLAvailabilityGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a3f-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c2a3f-125">-Name</span></span>
<span data-ttu-id="c2a3f-126">Указывает имя базы данных, экземпляра или AvailabilityGroup.</span><span class="sxs-lookup"><span data-stu-id="c2a3f-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterParamSet, IdParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a3f-127">-ParentID</span><span class="sxs-lookup"><span data-stu-id="c2a3f-127">-ParentID</span></span>
<span data-ttu-id="c2a3f-128">Указывает идентификатор ARM экземпляра или AG.</span><span class="sxs-lookup"><span data-stu-id="c2a3f-128">Specified the ARM ID of an Instance or AG.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a3f-129">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="c2a3f-129">-ServerName</span></span>
<span data-ttu-id="c2a3f-130">Указывает имя сервера, которому принадлежит элемент.</span><span class="sxs-lookup"><span data-stu-id="c2a3f-130">Specifies the name of the server to which the item belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterParamSet, IdParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a3f-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="c2a3f-131">-VaultId</span></span>
<span data-ttu-id="c2a3f-132">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="c2a3f-132">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a3f-133">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="c2a3f-133">-WorkloadType</span></span>
<span data-ttu-id="c2a3f-134">Тип рабочей нагрузки ресурса.</span><span class="sxs-lookup"><span data-stu-id="c2a3f-134">Workload type of the resource.</span></span> <span data-ttu-id="c2a3f-135">Текущие поддерживаемые значения — AzureVM, WindowsServer, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="c2a3f-135">The current supported values are  AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:
Accepted values: AzureVM, WindowsServer, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a3f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2a3f-136">CommonParameters</span></span>
<span data-ttu-id="c2a3f-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2a3f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2a3f-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2a3f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2a3f-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2a3f-139">INPUTS</span></span>

### <span data-ttu-id="c2a3f-140">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="c2a3f-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="c2a3f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c2a3f-141">System.String</span></span>

## <span data-ttu-id="c2a3f-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2a3f-142">OUTPUTS</span></span>

### <span data-ttu-id="c2a3f-143">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ProtectableItemBase</span><span class="sxs-lookup"><span data-stu-id="c2a3f-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="c2a3f-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2a3f-144">NOTES</span></span>

## <span data-ttu-id="c2a3f-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2a3f-145">RELATED LINKS</span></span>