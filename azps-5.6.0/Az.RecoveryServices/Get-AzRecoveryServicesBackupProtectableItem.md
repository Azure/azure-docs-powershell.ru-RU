---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 1d14a1559d62f00b4a513c6a25dad28b7816e2d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990867"
---
# <span data-ttu-id="bee3e-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="bee3e-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="bee3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bee3e-102">SYNOPSIS</span></span>
<span data-ttu-id="bee3e-103">Эта команда извлекает все защищенные элементы в определенном контейнере или во всех зарегистрированных контейнерах.</span><span class="sxs-lookup"><span data-stu-id="bee3e-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="bee3e-104">Она будет состоять из всех элементов иерархии приложения.</span><span class="sxs-lookup"><span data-stu-id="bee3e-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="bee3e-105">Возвращает DBS и их объекты верхнего уровня, такие как Instance, AvailabilityGroup и т. д.</span><span class="sxs-lookup"><span data-stu-id="bee3e-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="bee3e-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bee3e-106">SYNTAX</span></span>

### <span data-ttu-id="bee3e-107">NoFilterParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bee3e-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bee3e-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="bee3e-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bee3e-109">IdParamSet</span><span class="sxs-lookup"><span data-stu-id="bee3e-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bee3e-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bee3e-110">DESCRIPTION</span></span>
<span data-ttu-id="bee3e-111">Для получения списка защищенных элементов в контейнере и состояния защиты для них возвращается список **get-AzRecoveryServicesBackupProtectableItem.**</span><span class="sxs-lookup"><span data-stu-id="bee3e-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the list of protectable items in a container and the protection status of the items.</span></span>
<span data-ttu-id="bee3e-112">Контейнер, зарегистрированный в хранилище служб восстановления Azure, может иметь один или несколько элементов, которые можно защитить.</span><span class="sxs-lookup"><span data-stu-id="bee3e-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="bee3e-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bee3e-113">EXAMPLES</span></span>

### <span data-ttu-id="bee3e-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bee3e-114">Example 1</span></span>
```
PS C:\> $Vault = Get-AzRecoveryServicesVault -Name "MyRecoveryVault"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer -Status Registered -VaultId $Vault.Id
PS C:\> $Item = Get-AzRecoveryServicesBackupProtectableItem -Container $Container -ItemType "SQLInstance" -WorkloadType "MSSQL" -VaultId $Vault.ID
```

<span data-ttu-id="bee3e-115">Первая команда получает контейнер типа MSSQL, а затем сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="bee3e-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="bee3e-116">Вторая команда получает защищенный элемент резервной копии в $Container, а затем сохраняет его в $Item переменной.</span><span class="sxs-lookup"><span data-stu-id="bee3e-116">The second command gets the Backup protectable item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="bee3e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bee3e-117">PARAMETERS</span></span>

### <span data-ttu-id="bee3e-118">-Container</span><span class="sxs-lookup"><span data-stu-id="bee3e-118">-Container</span></span>
<span data-ttu-id="bee3e-119">Контейнер, в котором находится элемент</span><span class="sxs-lookup"><span data-stu-id="bee3e-119">Container where the item resides</span></span>

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

### <span data-ttu-id="bee3e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bee3e-120">-DefaultProfile</span></span>
<span data-ttu-id="bee3e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bee3e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bee3e-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="bee3e-122">-ItemType</span></span>
<span data-ttu-id="bee3e-123">Определяет тип защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="bee3e-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="bee3e-124">Применимые значения: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span><span class="sxs-lookup"><span data-stu-id="bee3e-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

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

### <span data-ttu-id="bee3e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="bee3e-125">-Name</span></span>
<span data-ttu-id="bee3e-126">Имя базы данных, экземпляра или группы доступности.</span><span class="sxs-lookup"><span data-stu-id="bee3e-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

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

### <span data-ttu-id="bee3e-127">-ParentID</span><span class="sxs-lookup"><span data-stu-id="bee3e-127">-ParentID</span></span>
<span data-ttu-id="bee3e-128">Определяет ARM экземпляра или AG.</span><span class="sxs-lookup"><span data-stu-id="bee3e-128">Specified the ARM ID of an Instance or AG.</span></span>

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

### <span data-ttu-id="bee3e-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bee3e-129">-ServerName</span></span>
<span data-ttu-id="bee3e-130">Имя сервера, к которому относится элемент.</span><span class="sxs-lookup"><span data-stu-id="bee3e-130">Specifies the name of the server to which the item belongs.</span></span>

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

### <span data-ttu-id="bee3e-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="bee3e-131">-VaultId</span></span>
<span data-ttu-id="bee3e-132">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="bee3e-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="bee3e-133">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="bee3e-133">-WorkloadType</span></span>
<span data-ttu-id="bee3e-134">Тип рабочей нагрузки ресурса.</span><span class="sxs-lookup"><span data-stu-id="bee3e-134">Workload type of the resource.</span></span> <span data-ttu-id="bee3e-135">В настоящее время поддерживаются значения AzureVM, WindowsServer, AzureFiles, MSSQL.</span><span class="sxs-lookup"><span data-stu-id="bee3e-135">The current supported values are  AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="bee3e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bee3e-136">CommonParameters</span></span>
<span data-ttu-id="bee3e-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bee3e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bee3e-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bee3e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bee3e-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bee3e-139">INPUTS</span></span>

### <span data-ttu-id="bee3e-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="bee3e-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="bee3e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="bee3e-141">System.String</span></span>

## <span data-ttu-id="bee3e-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bee3e-142">OUTPUTS</span></span>

### <span data-ttu-id="bee3e-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span><span class="sxs-lookup"><span data-stu-id="bee3e-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="bee3e-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bee3e-144">NOTES</span></span>

## <span data-ttu-id="bee3e-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bee3e-145">RELATED LINKS</span></span>
