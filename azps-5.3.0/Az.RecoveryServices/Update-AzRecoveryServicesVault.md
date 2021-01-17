---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
ms.openlocfilehash: cdde8169c4b068b986910dc3bfc5de446833f5ff
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421228"
---
# <span data-ttu-id="5b377-101">Update-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="5b377-101">Update-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="5b377-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b377-102">SYNOPSIS</span></span>
<span data-ttu-id="5b377-103">Обновляет MSI-версию хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="5b377-103">Updates MSI to the recovery services vault.</span></span>

## <span data-ttu-id="5b377-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5b377-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesVault -ResourceGroupName <string> -Name <string> -IdentityType <MSIdentity>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b377-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b377-105">DESCRIPTION</span></span>
<span data-ttu-id="5b377-106">Этот cmdlet используется для добавления или удаления MSI-данных из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="5b377-106">This cmdlet is used to add or remove  the MSI from the recovery services vault.</span></span> <span data-ttu-id="5b377-107">Используйте параметр -IdentityType, чтобы назначить удостоверение SystemAssigned RSVault.</span><span class="sxs-lookup"><span data-stu-id="5b377-107">Use -IdentityType param to assign a SystemAssigned identity to the RSVault.</span></span> <span data-ttu-id="5b377-108">Используйте IdentityType None, чтобы удалить MSI из хранилища.</span><span class="sxs-lookup"><span data-stu-id="5b377-108">Use IdentityType None to remove the MSI from the vault.</span></span>

## <span data-ttu-id="5b377-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5b377-109">EXAMPLES</span></span>

### <span data-ttu-id="5b377-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5b377-110">Example 1</span></span>
```powershell
PS C:\> Update-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName" -IdentityType SystemAssigned
```

<span data-ttu-id="5b377-111">Этот cmdlet используется для добавления удостоверения SystemAssigned в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="5b377-111">This cmdlet is used to add a SystemAssigned identity to a recovery services vault.</span></span>

## <span data-ttu-id="5b377-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b377-112">PARAMETERS</span></span>

### <span data-ttu-id="5b377-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b377-113">-DefaultProfile</span></span>
<span data-ttu-id="5b377-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b377-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b377-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5b377-115">-Name</span></span>

<span data-ttu-id="5b377-116">Указывает имя хранилища служб восстановления, которое нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="5b377-116">Specifies the name of the recovery services vault to update.</span></span>

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

### <span data-ttu-id="5b377-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b377-117">-ResourceGroupName</span></span>

<span data-ttu-id="5b377-118">Имя группы ресурсов Azure, в которой находится хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="5b377-118">Specifies the name of the Azure resource group where recovery services vault is present.</span></span>

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

### <span data-ttu-id="5b377-119">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="5b377-119">-IdentityType</span></span>
<span data-ttu-id="5b377-120">Тип MSI, присвоенный сейфу служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="5b377-120">The MSI type assigned to Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5b377-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b377-121">-Confirm</span></span>
<span data-ttu-id="5b377-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b377-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b377-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b377-123">-WhatIf</span></span>
<span data-ttu-id="5b377-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b377-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b377-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5b377-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b377-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b377-126">CommonParameters</span></span>
<span data-ttu-id="5b377-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b377-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b377-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b377-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b377-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b377-129">INPUTS</span></span>

### <span data-ttu-id="5b377-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5b377-130">System.String</span></span>

## <span data-ttu-id="5b377-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5b377-131">OUTPUTS</span></span>

### <span data-ttu-id="5b377-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span><span class="sxs-lookup"><span data-stu-id="5b377-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span></span>

## <span data-ttu-id="5b377-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5b377-133">NOTES</span></span>

## <span data-ttu-id="5b377-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b377-134">RELATED LINKS</span></span>
