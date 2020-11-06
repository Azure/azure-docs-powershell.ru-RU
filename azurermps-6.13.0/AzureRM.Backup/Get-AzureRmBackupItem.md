---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 8A638FB1-F530-4E28-BAAE-5382671092C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
ms.openlocfilehash: f0380a518353c3bc462a8a7b58012871359569a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563136"
---
# <span data-ttu-id="23d7b-101">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="23d7b-101">Get-AzureRmBackupItem</span></span>

## <span data-ttu-id="23d7b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23d7b-102">SYNOPSIS</span></span>
<span data-ttu-id="23d7b-103">Получает элементы в контейнере в резервной копии.</span><span class="sxs-lookup"><span data-stu-id="23d7b-103">Gets the items under a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23d7b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23d7b-104">SYNTAX</span></span>

```
Get-AzureRmBackupItem [-ProtectionStatus <String>] [-Status <String>] [-Type <String>]
 [-Container] <AzureRMBackupContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23d7b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23d7b-105">DESCRIPTION</span></span>
<span data-ttu-id="23d7b-106">Командлет **Get-AzureRmBackupItem** получает элементы в контейнере в резервной копии Azure и состояние защиты элементов.</span><span class="sxs-lookup"><span data-stu-id="23d7b-106">The **Get-AzureRmBackupItem** cmdlet gets the items in a container in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="23d7b-107">Включите элементы для защиты с помощью командлета Enable-AzureRmBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="23d7b-107">Enable items for protection by using the Enable-AzureRmBackupProtection cmdlet.</span></span>
<span data-ttu-id="23d7b-108">Контейнер, который регистрируется в хранилище резервных копий, может содержать один или несколько элементов, которые можно защитить.</span><span class="sxs-lookup"><span data-stu-id="23d7b-108">A container that is registered to a Backup vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="23d7b-109">Для виртуальных машин Azure в контейнере виртуальных машин может быть только один элемент.</span><span class="sxs-lookup"><span data-stu-id="23d7b-109">For Azure virtual machines, there can be only one item in the virtual machine container.</span></span>

## <span data-ttu-id="23d7b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23d7b-110">EXAMPLES</span></span>

### <span data-ttu-id="23d7b-111">Пример 1: получение элементов в контейнере</span><span class="sxs-lookup"><span data-stu-id="23d7b-111">Example 1: Get the items in a container</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container
Name                    ProtectionStatus       DataSourceStatus       RecoveryPointsCount    ProtectionPolicyName
----                    ----------------       ----------------       -------------------    --------------------
co03-vm                 NotProtected                                  0
```

<span data-ttu-id="23d7b-112">Первая команда получает хранилище с именем Vault03 с помощью командлета Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="23d7b-112">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="23d7b-113">Команда сохраняет этот объект в переменной $Vault.</span><span class="sxs-lookup"><span data-stu-id="23d7b-113">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="23d7b-114">Вторая команда получает контейнер с указанным именем в хранилище $Vault с помощью командлета **Get-AzureRmBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="23d7b-114">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="23d7b-115">Команда сохраняет этот объект в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="23d7b-115">The command stores that object in the $Container variable.</span></span>
<span data-ttu-id="23d7b-116">Последняя команда получает элемент резервного копирования из контейнера в $Container.</span><span class="sxs-lookup"><span data-stu-id="23d7b-116">The final command gets the backup item in the container in $Container.</span></span>

### <span data-ttu-id="23d7b-117">Пример 2: Просмотр всех свойств элемента</span><span class="sxs-lookup"><span data-stu-id="23d7b-117">Example 2: View all properties for an item</span></span>
```
PS C:\>Get-AzureRmBackupItem -Container $Container | Select-Object -Property *
Name                 : co03-vm
DataSourceStatus     : 
ProtectionStatus     : NotProtected
Type                 : AzureVM
ProtectionPolicyName : 
ProtectionPolicyId   : 
RecoveryPointsCount  : 0
ItemName             : iaasvmcontainer;co03-vm;co03-vm
ContainerType        : AzureVM
ContainerUniqueName  : iaasvmcontainer;co03-vm;co03-vm
ResourceGroupName    : resourcegroup02
ResourceName         : vault03
Location             : southeastasia
```

<span data-ttu-id="23d7b-118">Эта команда возвращает элемент резервного копирования в контейнере в $Container, а затем передает его в командлет Select-Object.</span><span class="sxs-lookup"><span data-stu-id="23d7b-118">This command gets the backup item in the container in $Container, and then passes it to the Select-Object cmdlet.</span></span>
<span data-ttu-id="23d7b-119">Этот командлет возвращает все свойства элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="23d7b-119">That cmdlet returns all properties of the backup item.</span></span>
<span data-ttu-id="23d7b-120">Для получения дополнительных сведений введите `Get-Help Select-Object` .</span><span class="sxs-lookup"><span data-stu-id="23d7b-120">For more information, type `Get-Help Select-Object`.</span></span>

## <span data-ttu-id="23d7b-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23d7b-121">PARAMETERS</span></span>

### <span data-ttu-id="23d7b-122">-Container</span><span class="sxs-lookup"><span data-stu-id="23d7b-122">-Container</span></span>
<span data-ttu-id="23d7b-123">Указывает объект-контейнер, для которого этот командлет получает элементы резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="23d7b-123">Specifies a container object for which this cmdlet gets backup items.</span></span>
<span data-ttu-id="23d7b-124">Чтобы получить **AzureRmBackupContainer** , используйте командлет Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="23d7b-124">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23d7b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d7b-125">-DefaultProfile</span></span>
<span data-ttu-id="23d7b-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="23d7b-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23d7b-127">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="23d7b-127">-ProtectionStatus</span></span>
<span data-ttu-id="23d7b-128">Определяет общее состояние защиты элемента в контейнере.</span><span class="sxs-lookup"><span data-stu-id="23d7b-128">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="23d7b-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="23d7b-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="23d7b-130">Защищенного</span><span class="sxs-lookup"><span data-stu-id="23d7b-130">Protected</span></span> 
- <span data-ttu-id="23d7b-131">Обеспечения</span><span class="sxs-lookup"><span data-stu-id="23d7b-131">Protecting</span></span>  
- <span data-ttu-id="23d7b-132">NotProtected</span><span class="sxs-lookup"><span data-stu-id="23d7b-132">NotProtected</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Protected, Protecting, NotProtected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d7b-133">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="23d7b-133">-Status</span></span>
<span data-ttu-id="23d7b-134">Задает состояние резервного копирования для элемента.</span><span class="sxs-lookup"><span data-stu-id="23d7b-134">Specifies the backup status for an item.</span></span>
<span data-ttu-id="23d7b-135">Допустимые значения этого параметра: IRPending, protected, ProtectionError и ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="23d7b-135">The acceptable values for this parameter are: IRPending, Protected, ProtectionError, and ProtectionStopped.</span></span>
<span data-ttu-id="23d7b-136">Если параметр *ProtectionStatus* имеет значение protected, вы можете использовать значение параметра *Status* для фильтрации элементов.</span><span class="sxs-lookup"><span data-stu-id="23d7b-136">If the *ProtectionStatus* parameter has the value Protected, you can use the *Status* parameter value to filter items.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IRPending, ProtectionStopped, ProtectionError, Protected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d7b-137">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="23d7b-137">-Type</span></span>
<span data-ttu-id="23d7b-138">Указывает тип элемента, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="23d7b-138">Specifies the type of item that this cmdlet gets.</span></span>
<span data-ttu-id="23d7b-139">В настоящее время единственным поддерживаемым значением является значение AzureVM.</span><span class="sxs-lookup"><span data-stu-id="23d7b-139">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d7b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d7b-140">CommonParameters</span></span>
<span data-ttu-id="23d7b-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23d7b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d7b-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23d7b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d7b-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23d7b-143">INPUTS</span></span>

### <span data-ttu-id="23d7b-144">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupContainer</span><span class="sxs-lookup"><span data-stu-id="23d7b-144">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer</span></span>
<span data-ttu-id="23d7b-145">Параметры: Container (ByValue)</span><span class="sxs-lookup"><span data-stu-id="23d7b-145">Parameters: Container (ByValue)</span></span>

## <span data-ttu-id="23d7b-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23d7b-146">OUTPUTS</span></span>

### <span data-ttu-id="23d7b-147">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupItem</span><span class="sxs-lookup"><span data-stu-id="23d7b-147">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem</span></span>

## <span data-ttu-id="23d7b-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="23d7b-148">NOTES</span></span>

## <span data-ttu-id="23d7b-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23d7b-149">RELATED LINKS</span></span>

[<span data-ttu-id="23d7b-150">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="23d7b-150">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="23d7b-151">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="23d7b-151">Disable-AzureRmBackupProtection</span></span>](./Disable-AzureRmBackupProtection.md)

[<span data-ttu-id="23d7b-152">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="23d7b-152">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="23d7b-153">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="23d7b-153">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="23d7b-154">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="23d7b-154">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="23d7b-155">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="23d7b-155">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)


