---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/remove-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: e6ac59a84e4244cb6d6815f8e3256618cccd661c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568419"
---
# <span data-ttu-id="cd8dc-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="cd8dc-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="cd8dc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd8dc-102">SYNOPSIS</span></span>
<span data-ttu-id="cd8dc-103">Удаляет хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="cd8dc-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd8dc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd8dc-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd8dc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd8dc-105">DESCRIPTION</span></span>
<span data-ttu-id="cd8dc-106">Командлет **Remove-AzureRmRecoveryServicesVault** удаляет хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="cd8dc-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="cd8dc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd8dc-107">EXAMPLES</span></span>

### <span data-ttu-id="cd8dc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cd8dc-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="cd8dc-109">Удаляет хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="cd8dc-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="cd8dc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd8dc-110">PARAMETERS</span></span>

### <span data-ttu-id="cd8dc-111">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="cd8dc-111">-Vault</span></span>
<span data-ttu-id="cd8dc-112">Указывает объект хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cd8dc-112">Specifies an Azure Site Recovery vault object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd8dc-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd8dc-113">-Confirm</span></span>
<span data-ttu-id="cd8dc-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cd8dc-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd8dc-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd8dc-115">-WhatIf</span></span>
<span data-ttu-id="cd8dc-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cd8dc-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd8dc-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cd8dc-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd8dc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd8dc-118">-DefaultProfile</span></span>
<span data-ttu-id="cd8dc-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd8dc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd8dc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd8dc-120">CommonParameters</span></span>
<span data-ttu-id="cd8dc-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd8dc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd8dc-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd8dc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd8dc-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd8dc-123">INPUTS</span></span>

### <span data-ttu-id="cd8dc-124">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="cd8dc-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="cd8dc-125">Параметры: хранилище (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cd8dc-125">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="cd8dc-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd8dc-126">OUTPUTS</span></span>

### <span data-ttu-id="cd8dc-127">Microsoft. Azure. Commands. RecoveryServices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="cd8dc-127">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="cd8dc-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd8dc-128">NOTES</span></span>

## <span data-ttu-id="cd8dc-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd8dc-129">RELATED LINKS</span></span>

[<span data-ttu-id="cd8dc-130">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="cd8dc-130">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="cd8dc-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="cd8dc-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="cd8dc-132">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="cd8dc-132">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)


