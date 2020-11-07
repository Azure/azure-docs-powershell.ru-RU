---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: c11170e6bee80b9eaa19135ad604d8bf70e1baab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733475"
---
# <span data-ttu-id="3eeec-101">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="3eeec-101">Get-AzureRmBackupVault</span></span>

## <span data-ttu-id="3eeec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3eeec-102">SYNOPSIS</span></span>
<span data-ttu-id="3eeec-103">Возвращает хранилище резервных копий.</span><span class="sxs-lookup"><span data-stu-id="3eeec-103">Gets Backup vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3eeec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3eeec-104">SYNTAX</span></span>

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3eeec-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3eeec-105">DESCRIPTION</span></span>
<span data-ttu-id="3eeec-106">Командлет **Get-AzureRmBackupVault** получает резервные хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3eeec-106">The **Get-AzureRmBackupVault** cmdlet gets Azure Backup vaults.</span></span>
<span data-ttu-id="3eeec-107">Этот командлет возвращает объекты **AzureRmBackupVault** для использования с другими командлетами.</span><span class="sxs-lookup"><span data-stu-id="3eeec-107">This cmdlet returns **AzureRmBackupVault** objects for use with other cmdlets.</span></span>

## <span data-ttu-id="3eeec-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3eeec-108">EXAMPLES</span></span>

### <span data-ttu-id="3eeec-109">Пример 1: Просмотр всех резервных хранилищ</span><span class="sxs-lookup"><span data-stu-id="3eeec-109">Example 1: View all the Backup vaults</span></span>
```
PS C:\>Get-AzureRmBackupVault
```

<span data-ttu-id="3eeec-110">Эта команда получает все резервные хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3eeec-110">This command gets all the Azure Backup vaults.</span></span>

### <span data-ttu-id="3eeec-111">Пример 2: Просмотр всех хранилищ, созданных в Запад США</span><span class="sxs-lookup"><span data-stu-id="3eeec-111">Example 2: View all vaults created in West US</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

<span data-ttu-id="3eeec-112">Эта команда возвращает все резервные хранилища.</span><span class="sxs-lookup"><span data-stu-id="3eeec-112">This command gets all the Backup vaults.</span></span>
<span data-ttu-id="3eeec-113">Команда передает их в командлет Where-Object с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="3eeec-113">The command passes them to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3eeec-114">Этот командлет фильтрует результаты, основываясь на свойстве **Region** .</span><span class="sxs-lookup"><span data-stu-id="3eeec-114">That cmdlet filters the results based on the **Region** property.</span></span>
<span data-ttu-id="3eeec-115">Для получения дополнительных сведений введите `Get-Help Where-Object` .</span><span class="sxs-lookup"><span data-stu-id="3eeec-115">For more information, type `Get-Help Where-Object`.</span></span>

### <span data-ttu-id="3eeec-116">Пример 3: получение определенного хранилища</span><span class="sxs-lookup"><span data-stu-id="3eeec-116">Example 3: Get a specific vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="3eeec-117">Эта команда получает хранилище с именем Vault03.</span><span class="sxs-lookup"><span data-stu-id="3eeec-117">This command gets the vault named Vault03.</span></span>

### <span data-ttu-id="3eeec-118">Пример 4: подсчет количества хранилищ с локально избыточным хранилищем</span><span class="sxs-lookup"><span data-stu-id="3eeec-118">Example 4: Count the number of vaults that have locally redundant storage</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

<span data-ttu-id="3eeec-119">Эта команда получает все резервные хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3eeec-119">This command gets all the Azure Backup vaults.</span></span>
<span data-ttu-id="3eeec-120">Команда передает их в **Where-Object** , который фильтрует результаты на основе свойства **Storage** .</span><span class="sxs-lookup"><span data-stu-id="3eeec-120">The command passes them to **Where-Object** , which filters the results based on the **Storage** property.</span></span>
<span data-ttu-id="3eeec-121">Команда передается командлету Measure-Object, который содержит значение "LocallyRedundant", в котором учитываются результаты.</span><span class="sxs-lookup"><span data-stu-id="3eeec-121">The command passes the ones that have a value of LocallyRedundant to the Measure-Object cmdlet, which counts the results.</span></span>
<span data-ttu-id="3eeec-122">Для получения дополнительных сведений введите `Get-Help Measure-Object` .</span><span class="sxs-lookup"><span data-stu-id="3eeec-122">For more information, type `Get-Help Measure-Object`.</span></span>

## <span data-ttu-id="3eeec-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3eeec-123">PARAMETERS</span></span>

### <span data-ttu-id="3eeec-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eeec-124">-DefaultProfile</span></span>
<span data-ttu-id="3eeec-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3eeec-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3eeec-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3eeec-126">-Name</span></span>
<span data-ttu-id="3eeec-127">Указывает имя хранилища резервных копий, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3eeec-127">Specifies the name of the Backup vault that this cmdlet gets.</span></span>
<span data-ttu-id="3eeec-128">Если несколько хранилищ резервных копий имеют одинаковое имя, этот командлет возвращает их все.</span><span class="sxs-lookup"><span data-stu-id="3eeec-128">If more than one Backup vault has the same name, this cmdlet returns them all.</span></span>
<span data-ttu-id="3eeec-129">Укажите параметр *ResourceGroupName* , чтобы получить уникальное хранилище.</span><span class="sxs-lookup"><span data-stu-id="3eeec-129">Specify the *ResourceGroupName* parameter to get a unique vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eeec-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eeec-130">-ResourceGroupName</span></span>
<span data-ttu-id="3eeec-131">Указывает имя группы ресурсов Azure, в которой этот командлет получает резервное хранилище.</span><span class="sxs-lookup"><span data-stu-id="3eeec-131">Specifies the name of an Azure resource group in which this cmdlet gets a Backup vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eeec-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eeec-132">CommonParameters</span></span>
<span data-ttu-id="3eeec-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3eeec-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eeec-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eeec-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eeec-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3eeec-135">INPUTS</span></span>

### <span data-ttu-id="3eeec-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="3eeec-136">None</span></span>

## <span data-ttu-id="3eeec-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3eeec-137">OUTPUTS</span></span>

### <span data-ttu-id="3eeec-138">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="3eeec-138">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>

## <span data-ttu-id="3eeec-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="3eeec-139">NOTES</span></span>

## <span data-ttu-id="3eeec-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3eeec-140">RELATED LINKS</span></span>

[<span data-ttu-id="3eeec-141">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="3eeec-141">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="3eeec-142">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="3eeec-142">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="3eeec-143">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="3eeec-143">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="3eeec-144">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="3eeec-144">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


