---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: 4e6dab95f110e25f24781b2ffbd01a016bdaa9fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248023"
---
# <span data-ttu-id="85ba4-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="85ba4-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="85ba4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="85ba4-102">SYNOPSIS</span></span>
<span data-ttu-id="85ba4-103">Удаляет хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="85ba4-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="85ba4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="85ba4-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85ba4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85ba4-105">DESCRIPTION</span></span>
<span data-ttu-id="85ba4-106">Командлет **Remove-AzRecoveryServicesVault** удаляет хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="85ba4-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="85ba4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="85ba4-107">EXAMPLES</span></span>

### <span data-ttu-id="85ba4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="85ba4-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="85ba4-109">Удаляет хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="85ba4-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="85ba4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="85ba4-110">PARAMETERS</span></span>

### <span data-ttu-id="85ba4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85ba4-111">-DefaultProfile</span></span>
<span data-ttu-id="85ba4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85ba4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85ba4-113">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="85ba4-113">-Vault</span></span>
<span data-ttu-id="85ba4-114">Указывает объект хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="85ba4-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="85ba4-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85ba4-115">-Confirm</span></span>
<span data-ttu-id="85ba4-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="85ba4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85ba4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85ba4-117">-WhatIf</span></span>
<span data-ttu-id="85ba4-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="85ba4-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85ba4-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="85ba4-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85ba4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85ba4-120">CommonParameters</span></span>
<span data-ttu-id="85ba4-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="85ba4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85ba4-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85ba4-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85ba4-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="85ba4-123">INPUTS</span></span>

### <span data-ttu-id="85ba4-124">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="85ba4-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="85ba4-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="85ba4-125">OUTPUTS</span></span>

### <span data-ttu-id="85ba4-126">Microsoft. Azure. Commands. RecoveryServices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="85ba4-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="85ba4-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="85ba4-127">NOTES</span></span>

## <span data-ttu-id="85ba4-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85ba4-128">RELATED LINKS</span></span>

[<span data-ttu-id="85ba4-129">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="85ba4-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="85ba4-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="85ba4-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="85ba4-131">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="85ba4-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


