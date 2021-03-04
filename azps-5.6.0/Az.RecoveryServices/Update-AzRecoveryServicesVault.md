---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
ms.openlocfilehash: 104bb05b4a01f5407c56e6c89de632a1ec5ab475
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970003"
---
# <span data-ttu-id="e0d83-101">Update-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e0d83-101">Update-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="e0d83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0d83-102">SYNOPSIS</span></span>
<span data-ttu-id="e0d83-103">Обновляет MSI-версию хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e0d83-103">Updates MSI to the recovery services vault.</span></span>

## <span data-ttu-id="e0d83-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e0d83-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesVault -ResourceGroupName <string> -Name <string> -IdentityType <MSIdentity>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0d83-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0d83-105">DESCRIPTION</span></span>
<span data-ttu-id="e0d83-106">Этот cmdlet используется для добавления или удаления MSI-данных из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e0d83-106">This cmdlet is used to add or remove  the MSI from the recovery services vault.</span></span> <span data-ttu-id="e0d83-107">Используйте параметр -IdentityType, чтобы назначить удостоверение SystemAssigned RSVault.</span><span class="sxs-lookup"><span data-stu-id="e0d83-107">Use -IdentityType param to assign a SystemAssigned identity to the RSVault.</span></span> <span data-ttu-id="e0d83-108">Используйте IdentityType None, чтобы удалить MSI из хранилища.</span><span class="sxs-lookup"><span data-stu-id="e0d83-108">Use IdentityType None to remove the MSI from the vault.</span></span>

## <span data-ttu-id="e0d83-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e0d83-109">EXAMPLES</span></span>

### <span data-ttu-id="e0d83-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e0d83-110">Example 1</span></span>
```powershell
PS C:\> Update-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName" -IdentityType SystemAssigned
```

<span data-ttu-id="e0d83-111">Этот cmdlet используется для добавления удостоверения SystemAssigned в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e0d83-111">This cmdlet is used to add a SystemAssigned identity to a recovery services vault.</span></span>

## <span data-ttu-id="e0d83-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0d83-112">PARAMETERS</span></span>

### <span data-ttu-id="e0d83-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0d83-113">-DefaultProfile</span></span>
<span data-ttu-id="e0d83-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0d83-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d83-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e0d83-115">-Name</span></span>

<span data-ttu-id="e0d83-116">Указывает имя хранилища служб восстановления, которое нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="e0d83-116">Specifies the name of the recovery services vault to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d83-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0d83-117">-ResourceGroupName</span></span>

<span data-ttu-id="e0d83-118">Имя группы ресурсов Azure, в которой находится хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e0d83-118">Specifies the name of the Azure resource group where recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d83-119">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="e0d83-119">-IdentityType</span></span>
<span data-ttu-id="e0d83-120">Тип MSI, присвоенный сейфу служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e0d83-120">The MSI type assigned to Recovery Services Vault.</span></span>

```yaml
Type: MSIdentity
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d83-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0d83-121">-Confirm</span></span>
<span data-ttu-id="e0d83-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e0d83-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d83-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0d83-123">-WhatIf</span></span>
<span data-ttu-id="e0d83-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0d83-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0d83-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e0d83-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d83-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0d83-126">CommonParameters</span></span>
<span data-ttu-id="e0d83-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0d83-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0d83-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0d83-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0d83-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0d83-129">INPUTS</span></span>

### <span data-ttu-id="e0d83-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e0d83-130">System.String</span></span>

## <span data-ttu-id="e0d83-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e0d83-131">OUTPUTS</span></span>

### <span data-ttu-id="e0d83-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span><span class="sxs-lookup"><span data-stu-id="e0d83-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span></span>

## <span data-ttu-id="e0d83-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e0d83-133">NOTES</span></span>

## <span data-ttu-id="e0d83-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0d83-134">RELATED LINKS</span></span>
