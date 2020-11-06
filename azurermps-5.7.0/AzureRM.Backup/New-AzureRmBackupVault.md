---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 015E3BC9-C535-4EA2-8A30-C728385DBFF8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
ms.openlocfilehash: 77c2df1ec61b42aaded458bea564cf6c953c90ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567458"
---
# <span data-ttu-id="946ec-101">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="946ec-101">New-AzureRmBackupVault</span></span>

## <span data-ttu-id="946ec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="946ec-102">SYNOPSIS</span></span>
<span data-ttu-id="946ec-103">Создание резервного хранилища.</span><span class="sxs-lookup"><span data-stu-id="946ec-103">Creates a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="946ec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="946ec-104">SYNTAX</span></span>

```
New-AzureRmBackupVault [-ResourceGroupName] <String> [-Name] <String> [-Region] <String>
 [[-Storage] <AzureBackupVaultStorageType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="946ec-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="946ec-105">DESCRIPTION</span></span>
<span data-ttu-id="946ec-106">Командлет **New-AzureRmBackupVault** создает хранилище архивации Azure.</span><span class="sxs-lookup"><span data-stu-id="946ec-106">The **New-AzureRmBackupVault** cmdlet creates an Azure Backup vault.</span></span>
<span data-ttu-id="946ec-107">Этот командлет возвращает объект **AzureRmBackupVault** , который выступает в качестве ссылки на сущность хранилища.</span><span class="sxs-lookup"><span data-stu-id="946ec-107">This cmdlet returns an **AzureRmBackupVault** object that acts as a reference to the vault entity.</span></span>

## <span data-ttu-id="946ec-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="946ec-108">EXAMPLES</span></span>

### <span data-ttu-id="946ec-109">Пример 1: создание резервного хранилища</span><span class="sxs-lookup"><span data-stu-id="946ec-109">Example 1: Create a backup vault</span></span>
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup01" -Name "Vault03" -Region "westus"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup01/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="946ec-110">Эта команда создает хранилище резервных копий Azure с именем Vault03.</span><span class="sxs-lookup"><span data-stu-id="946ec-110">This command creates an Azure Backup vault named Vault03.</span></span>
<span data-ttu-id="946ec-111">Хранилище находится в группе ресурсов с именем ResourceGroup01 в регионе Западная часть США.</span><span class="sxs-lookup"><span data-stu-id="946ec-111">The vault is in the resource group named ResourceGroup01 in the West US region.</span></span>
<span data-ttu-id="946ec-112">Хранилище использует тип хранилища с геоизбыточностью по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="946ec-112">The vault uses the default GeoRedundant storage type.</span></span>

### <span data-ttu-id="946ec-113">Пример 2: создание хранилища резервных копий, использующего локально избыточное хранилище</span><span class="sxs-lookup"><span data-stu-id="946ec-113">Example 2: Create a backup vault that uses locally redundant storage</span></span>
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup02" -Name "Vault03" -Region "westus" -Storage LocallyRedundant
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup02/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup02
Region            : westus
Storage           : LocallyRedundant
```

<span data-ttu-id="946ec-114">Эта команда создает хранилище резервных копий Azure с именем Vault03.</span><span class="sxs-lookup"><span data-stu-id="946ec-114">This command creates an Azure Backup vault named Vault03.</span></span>
<span data-ttu-id="946ec-115">Хранилище находится в группе ресурсов с именем ResourceGroup02 в регионе Западная часть США.</span><span class="sxs-lookup"><span data-stu-id="946ec-115">The vault is in the resource group named ResourceGroup02 in the West US region.</span></span>
<span data-ttu-id="946ec-116">Хранилище использует тип хранилища LocallyRedundant.</span><span class="sxs-lookup"><span data-stu-id="946ec-116">The vault uses the LocallyRedundant storage type.</span></span>

## <span data-ttu-id="946ec-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="946ec-117">PARAMETERS</span></span>

### <span data-ttu-id="946ec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="946ec-118">-DefaultProfile</span></span>
<span data-ttu-id="946ec-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="946ec-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="946ec-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="946ec-120">-Name</span></span>
<span data-ttu-id="946ec-121">Указывает имя для хранилища резервных копий Azure.</span><span class="sxs-lookup"><span data-stu-id="946ec-121">Specifies a name for the Azure Backup vault.</span></span>
<span data-ttu-id="946ec-122">Имя должно быть уникальным в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="946ec-122">The name must be unique in a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="946ec-123">-Region (регион)</span><span class="sxs-lookup"><span data-stu-id="946ec-123">-Region</span></span>
<span data-ttu-id="946ec-124">Указывает регион Azure, в котором существует резервное хранилище.</span><span class="sxs-lookup"><span data-stu-id="946ec-124">Specifies an Azure region in which the backup vault exists.</span></span>
<span data-ttu-id="946ec-125">В сценариях гибридного резервного копирования рекомендуется создать хранилище в регионе, близком к локальному серверу, чтобы уменьшить задержку.</span><span class="sxs-lookup"><span data-stu-id="946ec-125">For hybrid backup scenarios, we recommend that you create a vault in a region close to the on-premise server to reduce latency.</span></span>
<span data-ttu-id="946ec-126">Для резервного копирования инфраструктуры Azure в качестве виртуальных машин служб (IaaS) хранилище становится точкой обнаружения локальных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="946ec-126">For backup of Azure infrastructure as a service (IaaS) virtual machines, the vault becomes the point of discovery for local virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="946ec-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="946ec-127">-ResourceGroupName</span></span>
<span data-ttu-id="946ec-128">Указывает имя существующей группы ресурсов Azure, в которой этот командлет создает резервное хранилище.</span><span class="sxs-lookup"><span data-stu-id="946ec-128">Specifies the name of an existing Azure resource group in which this cmdlet creates a Backup vault.</span></span>
<span data-ttu-id="946ec-129">Чтобы создать группу ресурсов, используйте командлет New-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="946ec-129">To create a resource group, use the New-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="946ec-130">Группа ресурсов и хранилище резервных копий Azure не должны находиться в одном регионе.</span><span class="sxs-lookup"><span data-stu-id="946ec-130">The resource group and the Azure Backup vault do not have to be in the same region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="946ec-131">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="946ec-131">-Storage</span></span>
<span data-ttu-id="946ec-132">Указывает тип хранения архивных данных.</span><span class="sxs-lookup"><span data-stu-id="946ec-132">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="946ec-133">Допустимые значения этого параметра: LocallyRedundant и геоизбыточный.</span><span class="sxs-lookup"><span data-stu-id="946ec-133">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>
<span data-ttu-id="946ec-134">Значение по умолчанию — геоизбыточное.</span><span class="sxs-lookup"><span data-stu-id="946ec-134">The default value is GeoRedundant.</span></span>

```yaml
Type: AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="946ec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="946ec-135">CommonParameters</span></span>
<span data-ttu-id="946ec-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="946ec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="946ec-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="946ec-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="946ec-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="946ec-138">INPUTS</span></span>

### <span data-ttu-id="946ec-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="946ec-139">None</span></span>

## <span data-ttu-id="946ec-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="946ec-140">OUTPUTS</span></span>

### <span data-ttu-id="946ec-141">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="946ec-141">AzureRmBackupVault</span></span>

## <span data-ttu-id="946ec-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="946ec-142">NOTES</span></span>
* <span data-ttu-id="946ec-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="946ec-143">None</span></span>

## <span data-ttu-id="946ec-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="946ec-144">RELATED LINKS</span></span>

[<span data-ttu-id="946ec-145">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="946ec-145">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="946ec-146">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="946ec-146">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="946ec-147">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="946ec-147">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


