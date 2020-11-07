---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 922BEA08-6619-4D4C-86EC-58279C9E1D93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
ms.openlocfilehash: 41209f3790b7520c50e3105f9ca7c4a5a0e79dfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734908"
---
# <span data-ttu-id="49c65-101">Unregister-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="49c65-101">Unregister-AzureRmBackupContainer</span></span>

## <span data-ttu-id="49c65-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49c65-102">SYNOPSIS</span></span>
<span data-ttu-id="49c65-103">Отмена регистрации контейнера из резервного хранилища.</span><span class="sxs-lookup"><span data-stu-id="49c65-103">Unregisters a container from a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49c65-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49c65-104">SYNTAX</span></span>

```
Unregister-AzureRmBackupContainer [-Force] [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49c65-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49c65-105">DESCRIPTION</span></span>
<span data-ttu-id="49c65-106">Командлет **Unregister-AzureRmBackupContainer** отменяет регистрацию виртуальной машины Windows Server или Azure из резервного хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="49c65-106">The **Unregister-AzureRmBackupContainer** cmdlet unregisters the Windows Server or Azure virtual machine from an Azure Backup vault.</span></span>
<span data-ttu-id="49c65-107">Этот командлет удаляет ссылки на контейнер из резервного хранилища.</span><span class="sxs-lookup"><span data-stu-id="49c65-107">This cmdlet removes references to a container from the Backup vault.</span></span>
<span data-ttu-id="49c65-108">Прежде чем можно будет отменить регистрацию контейнера, необходимо удалить все защищенные данные, связанные с этим контейнером.</span><span class="sxs-lookup"><span data-stu-id="49c65-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

## <span data-ttu-id="49c65-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49c65-109">EXAMPLES</span></span>

### <span data-ttu-id="49c65-110">Пример 1: Отмена регистрации сервера Windows</span><span class="sxs-lookup"><span data-stu-id="49c65-110">Example 1: Unregister a Windows Server</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type Windows -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmBackupContainer -Container $Container[0]
Unregister Server
This operation will delete all data in the backup vault that is associated with the server. Are you sure you want to unregister the server? 
[] Yes  [] No  [?] Help (default is "No"): Yes
```

<span data-ttu-id="49c65-111">Первая команда получает хранилище с именем Vault03 с помощью командлета Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="49c65-111">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="49c65-112">Команда сохраняет этот объект в переменной $Vault.</span><span class="sxs-lookup"><span data-stu-id="49c65-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="49c65-113">Вторая команда получает контейнер с указанным именем в хранилище $Vault с помощью командлета Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="49c65-113">The second command gets a container that has the specified name in the vault in $Vault by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="49c65-114">Команда сохраняет этот объект в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="49c65-114">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="49c65-115">Последняя команда удаляет регистрацию указанного сервера Windows из хранилища архивации Azure.</span><span class="sxs-lookup"><span data-stu-id="49c65-115">The final command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

### <span data-ttu-id="49c65-116">Пример 2: Отмена регистрации сервера Windows без подтверждения</span><span class="sxs-lookup"><span data-stu-id="49c65-116">Example 2: Unregister a Windows Server without confirmation</span></span>
```
PS C:\>Unregister-AzureRmBackupContainer -Container $Container[0] -Force
```

<span data-ttu-id="49c65-117">Эта команда отменяет регистрацию указанного сервера Windows из хранилища архивации Azure, как в первом примере.</span><span class="sxs-lookup"><span data-stu-id="49c65-117">This command unregisters the specified Windows Server from the Azure Backup vault, just as in the first example.</span></span>
<span data-ttu-id="49c65-118">Эта команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="49c65-118">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="49c65-119">Таким образом, команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="49c65-119">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="49c65-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49c65-120">PARAMETERS</span></span>

### <span data-ttu-id="49c65-121">-Container</span><span class="sxs-lookup"><span data-stu-id="49c65-121">-Container</span></span>
<span data-ttu-id="49c65-122">Указывает виртуальную машину Windows Server или Azure, которую этот командлет отменяет.</span><span class="sxs-lookup"><span data-stu-id="49c65-122">Specifies the Windows Server or Azure virtual machine that this cmdlet unregisters.</span></span>
<span data-ttu-id="49c65-123">Чтобы получить **AzureRmBackupContainer** , используйте командлет Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="49c65-123">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="49c65-124">-Force</span><span class="sxs-lookup"><span data-stu-id="49c65-124">-Force</span></span>
<span data-ttu-id="49c65-125">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="49c65-125">Forces the command to run without asking for user confirmation.</span></span>
<span data-ttu-id="49c65-126">Этот параметр относится только к объектам **AzureBackupContainer** типа Windows.</span><span class="sxs-lookup"><span data-stu-id="49c65-126">This parameter is relevant only for **AzureBackupContainer** objects of type Windows.</span></span>

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

### <span data-ttu-id="49c65-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49c65-127">-Confirm</span></span>
<span data-ttu-id="49c65-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="49c65-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49c65-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49c65-129">-WhatIf</span></span>
<span data-ttu-id="49c65-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="49c65-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49c65-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="49c65-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49c65-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49c65-132">-DefaultProfile</span></span>
<span data-ttu-id="49c65-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49c65-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49c65-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49c65-134">CommonParameters</span></span>
<span data-ttu-id="49c65-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49c65-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49c65-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49c65-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49c65-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49c65-137">INPUTS</span></span>

### <span data-ttu-id="49c65-138">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="49c65-138">AzureBackupContainer</span></span>

## <span data-ttu-id="49c65-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49c65-139">OUTPUTS</span></span>

### <span data-ttu-id="49c65-140">AzureBackupJob</span><span class="sxs-lookup"><span data-stu-id="49c65-140">AzureBackupJob</span></span>
<span data-ttu-id="49c65-141">Этот командлет возвращает $Null, если контейнером является тип Windows Server.</span><span class="sxs-lookup"><span data-stu-id="49c65-141">This cmdlet returns $Null if the container type is Windows Server.</span></span>

## <span data-ttu-id="49c65-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="49c65-142">NOTES</span></span>
* <span data-ttu-id="49c65-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="49c65-143">None</span></span>

## <span data-ttu-id="49c65-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49c65-144">RELATED LINKS</span></span>

[<span data-ttu-id="49c65-145">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="49c65-145">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="49c65-146">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="49c65-146">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="49c65-147">Регистрация — AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="49c65-147">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)


