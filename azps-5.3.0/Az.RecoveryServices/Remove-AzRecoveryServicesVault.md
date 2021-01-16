---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: 4e6dab95f110e25f24781b2ffbd01a016bdaa9fd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506741"
---
# <span data-ttu-id="0ac5b-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="0ac5b-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="0ac5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ac5b-102">SYNOPSIS</span></span>
<span data-ttu-id="0ac5b-103">Удаляет хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="0ac5b-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="0ac5b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0ac5b-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ac5b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ac5b-105">DESCRIPTION</span></span>
<span data-ttu-id="0ac5b-106">**Cmdlet Remove-AzRecoveryServicesVault** удаляет хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="0ac5b-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="0ac5b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0ac5b-107">EXAMPLES</span></span>

### <span data-ttu-id="0ac5b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0ac5b-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="0ac5b-109">Удаляет хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="0ac5b-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="0ac5b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ac5b-110">PARAMETERS</span></span>

### <span data-ttu-id="0ac5b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ac5b-111">-DefaultProfile</span></span>
<span data-ttu-id="0ac5b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ac5b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ac5b-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="0ac5b-113">-Vault</span></span>
<span data-ttu-id="0ac5b-114">Указывает объект хранилища для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="0ac5b-114">Specifies an Azure Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ac5b-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ac5b-115">-Confirm</span></span>
<span data-ttu-id="0ac5b-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ac5b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ac5b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ac5b-117">-WhatIf</span></span>
<span data-ttu-id="0ac5b-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ac5b-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ac5b-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0ac5b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ac5b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ac5b-120">CommonParameters</span></span>
<span data-ttu-id="0ac5b-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ac5b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ac5b-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ac5b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ac5b-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ac5b-123">INPUTS</span></span>

### <span data-ttu-id="0ac5b-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="0ac5b-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="0ac5b-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0ac5b-125">OUTPUTS</span></span>

### <span data-ttu-id="0ac5b-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="0ac5b-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="0ac5b-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0ac5b-127">NOTES</span></span>

## <span data-ttu-id="0ac5b-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ac5b-128">RELATED LINKS</span></span>

[<span data-ttu-id="0ac5b-129">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="0ac5b-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="0ac5b-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="0ac5b-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="0ac5b-131">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="0ac5b-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


