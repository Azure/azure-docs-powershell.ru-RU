---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 698DCD00-13C0-4C36-A74B-35215D608339
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/remove-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
ms.openlocfilehash: 883c4a9892f4525b15369dbb1c3ed6134eb29f00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561160"
---
# <span data-ttu-id="0838f-101">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="0838f-101">Remove-AzureRmBackupVault</span></span>

## <span data-ttu-id="0838f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0838f-102">SYNOPSIS</span></span>
<span data-ttu-id="0838f-103">Удаление резервного хранилища.</span><span class="sxs-lookup"><span data-stu-id="0838f-103">Deletes a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0838f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0838f-104">SYNTAX</span></span>

```
Remove-AzureRmBackupVault [-Force] [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0838f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0838f-105">DESCRIPTION</span></span>
<span data-ttu-id="0838f-106">Командлет **Remove-AzureRmBackupVault** удаляет хранилище архивации Azure.</span><span class="sxs-lookup"><span data-stu-id="0838f-106">The **Remove-AzureRmBackupVault** cmdlet deletes an Azure Backup vault.</span></span>
<span data-ttu-id="0838f-107">Перед удалением резервного хранилища оно должно быть пустым.</span><span class="sxs-lookup"><span data-stu-id="0838f-107">Before you can delete a Backup vault, it must be empty.</span></span>
<span data-ttu-id="0838f-108">С помощью командлета **Remove-AzureRmBackupContainer** удалите инфраструктуру в качестве данных резервной копии виртуальных машин (IaaS) для службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="0838f-108">Use the **Remove-AzureRmBackupContainer** cmdlet to remove infrastructure as a service (IaaS) virtual machine backup data from the vault.</span></span>
<span data-ttu-id="0838f-109">С помощью командлета **delete-registeredserver** можно удалить другие зарегистрированные серверы и данные резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="0838f-109">Use the **Delete-RegisteredServer** cmdlet to remove other registered servers and backup data.</span></span>

## <span data-ttu-id="0838f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0838f-110">EXAMPLES</span></span>

### <span data-ttu-id="0838f-111">Пример 1: Удаление хранилища резервных копий Azure</span><span class="sxs-lookup"><span data-stu-id="0838f-111">Example 1: Delete an Azure Backup vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Remove-AzureRmBackupVault
```

<span data-ttu-id="0838f-112">Эта команда получает хранилище резервных копий Azure с именем Vault03 с помощью командлета **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="0838f-112">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="0838f-113">Команда передает это хранилище в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="0838f-113">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0838f-114">Текущий командлет удаляет хранилище.</span><span class="sxs-lookup"><span data-stu-id="0838f-114">The current cmdlet removes the vault.</span></span>

## <span data-ttu-id="0838f-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0838f-115">PARAMETERS</span></span>

### <span data-ttu-id="0838f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0838f-116">-DefaultProfile</span></span>
<span data-ttu-id="0838f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0838f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0838f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0838f-118">-Force</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0838f-119">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="0838f-119">-Vault</span></span>
<span data-ttu-id="0838f-120">Указывает хранилище резервных копий, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0838f-120">Specifies a Backup vault that this cmdlet removes.</span></span>
<span data-ttu-id="0838f-121">Чтобы получить **AzureRmBackupVault** , используйте командлет Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="0838f-121">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="0838f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0838f-122">-Confirm</span></span>
<span data-ttu-id="0838f-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0838f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0838f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0838f-124">-WhatIf</span></span>
<span data-ttu-id="0838f-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0838f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0838f-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0838f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0838f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0838f-127">CommonParameters</span></span>
<span data-ttu-id="0838f-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0838f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0838f-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0838f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0838f-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0838f-130">INPUTS</span></span>

### <span data-ttu-id="0838f-131">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="0838f-131">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="0838f-132">Параметры: хранилище (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0838f-132">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="0838f-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0838f-133">OUTPUTS</span></span>

### <span data-ttu-id="0838f-134">System. void</span><span class="sxs-lookup"><span data-stu-id="0838f-134">System.Void</span></span>

## <span data-ttu-id="0838f-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="0838f-135">NOTES</span></span>
* <span data-ttu-id="0838f-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="0838f-136">None</span></span>

## <span data-ttu-id="0838f-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0838f-137">RELATED LINKS</span></span>

[<span data-ttu-id="0838f-138">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="0838f-138">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="0838f-139">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="0838f-139">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="0838f-140">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="0838f-140">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


