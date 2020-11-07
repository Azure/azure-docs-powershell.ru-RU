---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/unregister-azurermrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: 817f22343697d888ba1ce9a568ed0ce218b284e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732908"
---
# <span data-ttu-id="e64f3-101">Unregister-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e64f3-101">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="e64f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e64f3-102">SYNOPSIS</span></span>
<span data-ttu-id="e64f3-103">Отмена регистрации сервера Windows или другого контейнера из хранилища.</span><span class="sxs-lookup"><span data-stu-id="e64f3-103">Unregisters a Windows Server or other container from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e64f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e64f3-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupContainer [-Container] <ContainerBase> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e64f3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e64f3-105">DESCRIPTION</span></span>
<span data-ttu-id="e64f3-106">Командлет **Unregister-AzureRmRecoveryServicesBackupContainer** отменяет регистрацию сервера Windows или другого контейнера резервной копии из хранилища.</span><span class="sxs-lookup"><span data-stu-id="e64f3-106">The **Unregister-AzureRmRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="e64f3-107">Этот командлет удаляет ссылки на контейнер из хранилища.</span><span class="sxs-lookup"><span data-stu-id="e64f3-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="e64f3-108">Прежде чем можно будет отменить регистрацию контейнера, необходимо удалить все защищенные данные, связанные с этим контейнером.</span><span class="sxs-lookup"><span data-stu-id="e64f3-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="e64f3-109">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="e64f3-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="e64f3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e64f3-110">EXAMPLES</span></span>

### <span data-ttu-id="e64f3-111">Пример 1: Отмена регистрации сервера Windows из хранилища</span><span class="sxs-lookup"><span data-stu-id="e64f3-111">Example 1: Unregister a Windows Server from the vault</span></span>
```
PS C:\>$Cont = Get-AzureRmRecoveryServicesBackupContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="e64f3-112">Первая команда получает контейнер Windows с именем server01.contoso.com, который зарегистрирован в хранилище, и сохраняет его в переменной $Cont.</span><span class="sxs-lookup"><span data-stu-id="e64f3-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>
<span data-ttu-id="e64f3-113">Вторая команда удаляет регистрацию указанного сервера Windows из хранилища архивации Azure.</span><span class="sxs-lookup"><span data-stu-id="e64f3-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

## <span data-ttu-id="e64f3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e64f3-114">PARAMETERS</span></span>

### <span data-ttu-id="e64f3-115">-Container</span><span class="sxs-lookup"><span data-stu-id="e64f3-115">-Container</span></span>
<span data-ttu-id="e64f3-116">Указывает объект контейнера резервной копии, который нужно отменить.</span><span class="sxs-lookup"><span data-stu-id="e64f3-116">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="e64f3-117">Чтобы получить объект **BackupContainer** , используйте командлет Get-AzureRmRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="e64f3-117">To obtain a **BackupContainer** object, use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e64f3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e64f3-118">-DefaultProfile</span></span>
<span data-ttu-id="e64f3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e64f3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e64f3-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e64f3-120">-PassThru</span></span>
<span data-ttu-id="e64f3-121">Возвращает контейнер, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="e64f3-121">Return the container to be deleted.</span></span>

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

### <span data-ttu-id="e64f3-122">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e64f3-122">-VaultId</span></span>
<span data-ttu-id="e64f3-123">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e64f3-123">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e64f3-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e64f3-124">-Confirm</span></span>
<span data-ttu-id="e64f3-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e64f3-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e64f3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e64f3-126">-WhatIf</span></span>
<span data-ttu-id="e64f3-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e64f3-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e64f3-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e64f3-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e64f3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e64f3-129">CommonParameters</span></span>
<span data-ttu-id="e64f3-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e64f3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e64f3-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e64f3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e64f3-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e64f3-132">INPUTS</span></span>

### <span data-ttu-id="e64f3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e64f3-133">System.String</span></span>
<span data-ttu-id="e64f3-134">Параметры: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e64f3-134">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="e64f3-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e64f3-135">OUTPUTS</span></span>

### <span data-ttu-id="e64f3-136">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="e64f3-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="e64f3-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="e64f3-137">NOTES</span></span>

## <span data-ttu-id="e64f3-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e64f3-138">RELATED LINKS</span></span>

[<span data-ttu-id="e64f3-139">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e64f3-139">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)


