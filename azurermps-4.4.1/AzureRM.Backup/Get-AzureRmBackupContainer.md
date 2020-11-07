---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: c7bcddca0cfef631f7501dfb6c017f2c6ef7af25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732233"
---
# <span data-ttu-id="64509-101">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="64509-101">Get-AzureRmBackupContainer</span></span>

## <span data-ttu-id="64509-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="64509-102">SYNOPSIS</span></span>
<span data-ttu-id="64509-103">Получает контейнеры резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="64509-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64509-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="64509-104">SYNTAX</span></span>

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64509-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64509-105">DESCRIPTION</span></span>
<span data-ttu-id="64509-106">Командлет **Get-AzureRmBackupContainer** получает контейнеры архивации Azure.</span><span class="sxs-lookup"><span data-stu-id="64509-106">The **Get-AzureRmBackupContainer** cmdlet gets Azure Backup containers.</span></span>

<span data-ttu-id="64509-107">**AzureBackupContainer** инкапсулирует источники данных, защищенные элементы и точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="64509-107">An **AzureBackupContainer** encapsulates data sources, protected items, and recovery points.</span></span>
<span data-ttu-id="64509-108">**AzureBackupContainer** может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="64509-108">An **AzureBackupContainer** can be one of the following:</span></span> 

- <span data-ttu-id="64509-109">Компьютер с Windows Server</span><span class="sxs-lookup"><span data-stu-id="64509-109">A Windows Server computer</span></span>
- <span data-ttu-id="64509-110">Сервер System Center Data Protection Manager (SCDPM)</span><span class="sxs-lookup"><span data-stu-id="64509-110">A System Center Data Protection Manager (SCDPM) server</span></span> 
- <span data-ttu-id="64509-111">Инфраструктура Azure в качестве виртуальной машины службы (IaaS)</span><span class="sxs-lookup"><span data-stu-id="64509-111">An Azure infrastructure as a service (IaaS) virtual machine</span></span>

<span data-ttu-id="64509-112">Перед тем, как резервное копирование может создать резервную копию источника данных или элемента, необходимо зарегистрировать контейнер, содержащий его в службе архивации Azure.</span><span class="sxs-lookup"><span data-stu-id="64509-112">Before Backup can back up a data source or item, you must register the container that holds it with the Azure Backup service.</span></span>
<span data-ttu-id="64509-113">Для отправки резервных данных в резервное хранилище необходимо проверить подлинность контейнера.</span><span class="sxs-lookup"><span data-stu-id="64509-113">The container must be authenticated to send backup data to the Backup vault.</span></span>
<span data-ttu-id="64509-114">Для компьютеров с Windows Server и серверов SCDPM регистрация удерживается с полным доменным именем сервера.</span><span class="sxs-lookup"><span data-stu-id="64509-114">For Windows Server computers and SCDPM servers, the registration is held with the fully qualified domain name of the server.</span></span>

## <span data-ttu-id="64509-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="64509-115">EXAMPLES</span></span>

### <span data-ttu-id="64509-116">Пример 1: Просмотр всех серверов, зарегистрированных в хранилище</span><span class="sxs-lookup"><span data-stu-id="64509-116">Example 1: View all servers registered to a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

<span data-ttu-id="64509-117">Первая команда получает хранилище с именем Vault03 с помощью командлета **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="64509-117">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="64509-118">Команда сохраняет этот объект в переменной $Vault.</span><span class="sxs-lookup"><span data-stu-id="64509-118">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="64509-119">Вторая команда получает все контейнеры типа Windows из хранилища в $Vault.</span><span class="sxs-lookup"><span data-stu-id="64509-119">The second command gets all containers of type Windows from the vault in $Vault.</span></span>

### <span data-ttu-id="64509-120">Пример 2: получение определенного контейнера</span><span class="sxs-lookup"><span data-stu-id="64509-120">Example 2: Get a specific container</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

<span data-ttu-id="64509-121">Эта команда получает контейнер с именем DPMSERVER. CONTOSO.COM.</span><span class="sxs-lookup"><span data-stu-id="64509-121">This command gets the container named DPMSERVER.CONTOSO.COM.</span></span>
<span data-ttu-id="64509-122">Команда задает хранилище в $Vault и тип контейнера.</span><span class="sxs-lookup"><span data-stu-id="64509-122">The command specifies the vault in $Vault and the type of container.</span></span>

### <span data-ttu-id="64509-123">Пример 3: Просмотр всех зарегистрированных виртуальных машин Azure</span><span class="sxs-lookup"><span data-stu-id="64509-123">Example 3: View all registered Azure virtual machines</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

<span data-ttu-id="64509-124">Эта команда получает зарегистрированные виртуальные машины из хранилища в $Vault.</span><span class="sxs-lookup"><span data-stu-id="64509-124">This command gets the registered virtual machines from the vault in $Vault.</span></span>

## <span data-ttu-id="64509-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="64509-125">PARAMETERS</span></span>

### <span data-ttu-id="64509-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64509-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="64509-127">Указывает имя группы ресурсов, связанной с контейнером.</span><span class="sxs-lookup"><span data-stu-id="64509-127">Specifies the name of the resource group associated with the container.</span></span>
<span data-ttu-id="64509-128">Это имя совпадает со значением, которое вы указали для параметра *ServiceName* или *ResourceGroupName* командлета Register-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="64509-128">This name is the same value that you specified for the *ServiceName* or *ResourceGroupName* parameter of the Register-AzureRmBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="64509-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="64509-129">-Name</span></span>
<span data-ttu-id="64509-130">Указывает имя контейнера, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="64509-130">Specifies the name of the container that this cmdlet gets.</span></span>

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

### <span data-ttu-id="64509-131">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="64509-131">-Status</span></span>
<span data-ttu-id="64509-132">Указывает текущее состояние контейнеров, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="64509-132">Specifies the current status of the containers that this cmdlet gets.</span></span>
<span data-ttu-id="64509-133">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="64509-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64509-134">NotRegistered</span><span class="sxs-lookup"><span data-stu-id="64509-134">NotRegistered</span></span> 
- <span data-ttu-id="64509-135">Пользователь</span><span class="sxs-lookup"><span data-stu-id="64509-135">Registered</span></span> 
- <span data-ttu-id="64509-136">Регистрируя</span><span class="sxs-lookup"><span data-stu-id="64509-136">Registering</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerRegistrationStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Registered, Registering, NotRegistered

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64509-137">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="64509-137">-Type</span></span>
<span data-ttu-id="64509-138">Указывает тип контейнеров, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="64509-138">Specifies the type of containers that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, SCDPM, AzureVM, AzureBackupServer, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64509-139">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="64509-139">-Vault</span></span>
<span data-ttu-id="64509-140">Указывает хранилище резервных копий, из которого этот командлет получает контейнеры.</span><span class="sxs-lookup"><span data-stu-id="64509-140">Specifies a Backup vault from which this cmdlet gets containers.</span></span>
<span data-ttu-id="64509-141">Чтобы получить **AzureRmBackupVault** , используйте командлет Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="64509-141">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64509-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64509-142">-DefaultProfile</span></span>
<span data-ttu-id="64509-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="64509-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64509-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64509-144">CommonParameters</span></span>
<span data-ttu-id="64509-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="64509-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64509-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64509-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64509-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="64509-147">INPUTS</span></span>

### <span data-ttu-id="64509-148">AzureBackupVault</span><span class="sxs-lookup"><span data-stu-id="64509-148">AzureBackupVault</span></span>

## <span data-ttu-id="64509-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="64509-149">OUTPUTS</span></span>

### <span data-ttu-id="64509-150">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="64509-150">AzureBackupContainer</span></span>

## <span data-ttu-id="64509-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="64509-151">NOTES</span></span>
* <span data-ttu-id="64509-152">Ничего</span><span class="sxs-lookup"><span data-stu-id="64509-152">None</span></span>

## <span data-ttu-id="64509-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64509-153">RELATED LINKS</span></span>

[<span data-ttu-id="64509-154">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="64509-154">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="64509-155">Регистрация — AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="64509-155">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)

[<span data-ttu-id="64509-156">Отмена регистрации — AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="64509-156">Unregister-AzureRmBackupContainer</span></span>](./Unregister-AzureRmBackupContainer.md)


