---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 189E3DD8-AA43-4D4C-A873-971E0585E54E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/remove-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: b7eaa3ef0c0379a0799e4091a4e808415b2f9fdc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561164"
---
# <span data-ttu-id="b6666-101">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b6666-101">Remove-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="b6666-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b6666-102">SYNOPSIS</span></span>
<span data-ttu-id="b6666-103">Удаление политики из резервного хранилища.</span><span class="sxs-lookup"><span data-stu-id="b6666-103">Deletes a policy from a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6666-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b6666-104">SYNTAX</span></span>

```
Remove-AzureRmBackupProtectionPolicy [-Force] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6666-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6666-105">DESCRIPTION</span></span>
<span data-ttu-id="b6666-106">Командлет **Remove-AzureRmBackupProtectionPolicy** удаляет политику из хранилища резервных копий Azure.</span><span class="sxs-lookup"><span data-stu-id="b6666-106">The **Remove-AzureRmBackupProtectionPolicy** cmdlet deletes a policy from an Azure Backup vault.</span></span>
<span data-ttu-id="b6666-107">Прежде чем можно будет удалить политику защиты резервных копий, она не должна содержать ни одного связанного элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="b6666-107">Before you can delete a backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="b6666-108">Перед удалением политики убедитесь, что все связанные элементы связаны с какой – либо другой политикой.</span><span class="sxs-lookup"><span data-stu-id="b6666-108">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="b6666-109">Чтобы связать другую политику с элементом резервной копии, используйте командлет Enable-AzureRmBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="b6666-109">To associate another policy with a backup item, use the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="b6666-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b6666-110">EXAMPLES</span></span>

### <span data-ttu-id="b6666-111">Пример 1: Удаление политики защиты резервной копии</span><span class="sxs-lookup"><span data-stu-id="b6666-111">Example 1: Remove a backup protection policy</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DailyBackup" | Remove-AzureRmBackupProtectionPolicy
```

<span data-ttu-id="b6666-112">Первая команда получает хранилище с именем Vault03 с помощью командлета Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="b6666-112">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="b6666-113">Команда сохраняет этот объект в переменной $Vault.</span><span class="sxs-lookup"><span data-stu-id="b6666-113">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="b6666-114">Вторая команда создает политику хранения в течение 30 дней ежедневной сохранности, а затем сохраняет ее в переменной $Daily.</span><span class="sxs-lookup"><span data-stu-id="b6666-114">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>
<span data-ttu-id="b6666-115">Вторая команда получает политику защиты с именем DailyBackup в хранилище в $Vault с помощью командлета **Get-AzureRmBackupProtectionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="b6666-115">The second command gets the protection policy named DailyBackup in the vault in $Vault by using the **Get-AzureRmBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="b6666-116">Команда передает политику текущему командлету.</span><span class="sxs-lookup"><span data-stu-id="b6666-116">The command passes the policy to the current cmdlet.</span></span>
<span data-ttu-id="b6666-117">Этот командлет удаляет политику.</span><span class="sxs-lookup"><span data-stu-id="b6666-117">That cmdlet removes the policy.</span></span>

## <span data-ttu-id="b6666-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b6666-118">PARAMETERS</span></span>

### <span data-ttu-id="b6666-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6666-119">-DefaultProfile</span></span>
<span data-ttu-id="b6666-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b6666-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6666-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b6666-121">-Force</span></span>
<span data-ttu-id="b6666-122">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b6666-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6666-123">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b6666-123">-ProtectionPolicy</span></span>
<span data-ttu-id="b6666-124">Задает политику защиты, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b6666-124">Specifies protection policy that this cmdlet removes.</span></span>
<span data-ttu-id="b6666-125">Чтобы получить **AzureRmBackupProtectionPolicy** , используйте командлет Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b6666-125">To obtain an **AzureRmBackupProtectionPolicy** , use the Get-AzureRmBackupProtectionPolicy cmdlet</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6666-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6666-126">-Confirm</span></span>
<span data-ttu-id="b6666-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b6666-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6666-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6666-128">-WhatIf</span></span>
<span data-ttu-id="b6666-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b6666-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6666-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b6666-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6666-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6666-131">CommonParameters</span></span>
<span data-ttu-id="b6666-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b6666-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6666-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6666-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6666-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b6666-134">INPUTS</span></span>

### <span data-ttu-id="b6666-135">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b6666-135">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy</span></span>
<span data-ttu-id="b6666-136">Параметры: ProtectionPolicy (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b6666-136">Parameters: ProtectionPolicy (ByValue)</span></span>

## <span data-ttu-id="b6666-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6666-137">OUTPUTS</span></span>

### <span data-ttu-id="b6666-138">System. void</span><span class="sxs-lookup"><span data-stu-id="b6666-138">System.Void</span></span>

## <span data-ttu-id="b6666-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="b6666-139">NOTES</span></span>

## <span data-ttu-id="b6666-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6666-140">RELATED LINKS</span></span>

[<span data-ttu-id="b6666-141">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="b6666-141">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="b6666-142">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b6666-142">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="b6666-143">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b6666-143">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


