---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: B3B708C5-776E-4F1C-BA0B-492CD9057794
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 08cfb4279199455b14794a890b398fd954cb4cd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560524"
---
# <span data-ttu-id="ba59f-101">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ba59f-101">Get-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="ba59f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba59f-102">SYNOPSIS</span></span>
<span data-ttu-id="ba59f-103">Получает политики резервного копирования для резервного хранилища.</span><span class="sxs-lookup"><span data-stu-id="ba59f-103">Gets backup policies for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba59f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba59f-104">SYNTAX</span></span>

```
Get-AzureRmBackupProtectionPolicy [[-Name] <String>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba59f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba59f-105">DESCRIPTION</span></span>
<span data-ttu-id="ba59f-106">Командлет **Get-AzureRmBackupProtectionPolicy** получает политики резервного копирования для резервного хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ba59f-106">The **Get-AzureRmBackupProtectionPolicy** cmdlet gets backup policies for an Azure Backup vault.</span></span>

## <span data-ttu-id="ba59f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba59f-107">EXAMPLES</span></span>

### <span data-ttu-id="ba59f-108">Пример 1: Просмотр политик в хранилище</span><span class="sxs-lookup"><span data-stu-id="ba59f-108">Example 1: View the policies in a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault 
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
contoso01                 AzureVM            Daily              26-Aug-15 3:00:00 PM
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
DefaultPolicy             AzureVM            Daily              26-Aug-15 12:30:00 AM
WeeklyBkp                 AzureVM            Weekly             26-Aug-15 5:00:00 PM
contoso02                 AzureVM            Daily              26-Aug-15 3:00:00 PM
```

<span data-ttu-id="ba59f-109">Первая команда получает хранилище с именем Vault03 с помощью командлета **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="ba59f-109">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="ba59f-110">Команда сохраняет этот объект в переменной $Vault.</span><span class="sxs-lookup"><span data-stu-id="ba59f-110">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="ba59f-111">Вторая команда получает все политики защиты резервных копий для хранилища в $Vault.</span><span class="sxs-lookup"><span data-stu-id="ba59f-111">The second command gets all the Backup protection policies for the vault in $Vault.</span></span>

### <span data-ttu-id="ba59f-112">Пример 2: получение определенной политики из хранилища</span><span class="sxs-lookup"><span data-stu-id="ba59f-112">Example 2: Get a specific policy from a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DefaultPolicy             AzureVM            Daily              26-Aug-15 12:30:00 AM
```

<span data-ttu-id="ba59f-113">Первая команда получает хранилище с именем Vault03 с помощью командлета **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="ba59f-113">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="ba59f-114">Команда сохраняет этот объект в переменной $Vault.</span><span class="sxs-lookup"><span data-stu-id="ba59f-114">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="ba59f-115">Вторая команда получает политику защиты резервного копирования с именем DefaultPolicy для хранилища в $Vault.</span><span class="sxs-lookup"><span data-stu-id="ba59f-115">The second command gets the Backup protection policy named DefaultPolicy for the vault in $Vault.</span></span>

## <span data-ttu-id="ba59f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba59f-116">PARAMETERS</span></span>

### <span data-ttu-id="ba59f-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ba59f-117">-Name</span></span>
<span data-ttu-id="ba59f-118">Указывает имя политики, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ba59f-118">Specifies the name of the policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ba59f-119">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="ba59f-119">-Vault</span></span>
<span data-ttu-id="ba59f-120">Указывает хранилище резервных копий, для которого этот командлет получает политики.</span><span class="sxs-lookup"><span data-stu-id="ba59f-120">Specifies the Backup vault for which this cmdlet gets policies.</span></span>
<span data-ttu-id="ba59f-121">Чтобы получить объект **AzureRmBackupVault** , используйте командлет Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="ba59f-121">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="ba59f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba59f-122">-DefaultProfile</span></span>
<span data-ttu-id="ba59f-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba59f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba59f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba59f-124">CommonParameters</span></span>
<span data-ttu-id="ba59f-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba59f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba59f-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba59f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba59f-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba59f-127">INPUTS</span></span>

### <span data-ttu-id="ba59f-128">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="ba59f-128">AzureRmBackupVault</span></span>

## <span data-ttu-id="ba59f-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba59f-129">OUTPUTS</span></span>

### <span data-ttu-id="ba59f-130">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ba59f-130">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="ba59f-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba59f-131">NOTES</span></span>
* <span data-ttu-id="ba59f-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="ba59f-132">None</span></span>

## <span data-ttu-id="ba59f-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba59f-133">RELATED LINKS</span></span>

[<span data-ttu-id="ba59f-134">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="ba59f-134">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="ba59f-135">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="ba59f-135">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="ba59f-136">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ba59f-136">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="ba59f-137">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ba59f-137">Remove-AzureRmBackupProtectionPolicy</span></span>](./Remove-AzureRmBackupProtectionPolicy.md)


