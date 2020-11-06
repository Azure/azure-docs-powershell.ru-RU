---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/remove-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 4d3046827a7d3338833b0c8c788cfb7a9e18bc2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566926"
---
# <span data-ttu-id="a0af4-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a0af4-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="a0af4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a0af4-102">SYNOPSIS</span></span>
<span data-ttu-id="a0af4-103">Удаляет хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="a0af4-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0af4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a0af4-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0af4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0af4-105">DESCRIPTION</span></span>
<span data-ttu-id="a0af4-106">Командлет **Remove-AzureRmRecoveryServicesVault** удаляет хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="a0af4-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="a0af4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a0af4-107">EXAMPLES</span></span>

### <span data-ttu-id="a0af4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a0af4-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="a0af4-109">Удаляет хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="a0af4-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="a0af4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a0af4-110">PARAMETERS</span></span>

### <span data-ttu-id="a0af4-111">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="a0af4-111">-Vault</span></span>
<span data-ttu-id="a0af4-112">Указывает объект хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a0af4-112">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="a0af4-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0af4-113">-Confirm</span></span>
<span data-ttu-id="a0af4-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a0af4-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0af4-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0af4-115">-WhatIf</span></span>
<span data-ttu-id="a0af4-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a0af4-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0af4-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a0af4-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0af4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0af4-118">-DefaultProfile</span></span>
<span data-ttu-id="a0af4-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a0af4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0af4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0af4-120">CommonParameters</span></span>
<span data-ttu-id="a0af4-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a0af4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0af4-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0af4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0af4-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a0af4-123">INPUTS</span></span>

### <span data-ttu-id="a0af4-124">ARSVault</span><span class="sxs-lookup"><span data-stu-id="a0af4-124">ARSVault</span></span>
<span data-ttu-id="a0af4-125">Параметр "хранилище" принимает значение типа "ARSVault" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a0af4-125">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="a0af4-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0af4-126">OUTPUTS</span></span>

### <span data-ttu-id="a0af4-127">Microsoft. Azure. Commands. RecoveryServices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="a0af4-127">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="a0af4-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="a0af4-128">NOTES</span></span>

## <span data-ttu-id="a0af4-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0af4-129">RELATED LINKS</span></span>

[<span data-ttu-id="a0af4-130">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a0af4-130">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="a0af4-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="a0af4-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="a0af4-132">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a0af4-132">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)


