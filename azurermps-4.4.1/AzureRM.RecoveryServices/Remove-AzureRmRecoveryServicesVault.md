---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: b3df84865d29bbcf62074c1b1ed7f5586fb64fee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733640"
---
# <span data-ttu-id="4ba7a-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4ba7a-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="4ba7a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ba7a-102">SYNOPSIS</span></span>
<span data-ttu-id="4ba7a-103">Удаляет хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="4ba7a-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ba7a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ba7a-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ba7a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ba7a-105">DESCRIPTION</span></span>
<span data-ttu-id="4ba7a-106">Командлет **Remove-AzureRmRecoveryServicesVault** удаляет хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="4ba7a-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="4ba7a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ba7a-107">EXAMPLES</span></span>

## <span data-ttu-id="4ba7a-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ba7a-108">PARAMETERS</span></span>

### <span data-ttu-id="4ba7a-109">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="4ba7a-109">-Vault</span></span>
<span data-ttu-id="4ba7a-110">Указывает объект хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4ba7a-110">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="4ba7a-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ba7a-111">-Confirm</span></span>
<span data-ttu-id="4ba7a-112">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4ba7a-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ba7a-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ba7a-113">-WhatIf</span></span>
<span data-ttu-id="4ba7a-114">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4ba7a-114">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ba7a-115">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4ba7a-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ba7a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ba7a-116">-DefaultProfile</span></span>
<span data-ttu-id="4ba7a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ba7a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ba7a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ba7a-118">CommonParameters</span></span>
<span data-ttu-id="4ba7a-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ba7a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ba7a-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ba7a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ba7a-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ba7a-121">INPUTS</span></span>

### <span data-ttu-id="4ba7a-122">ARSVault</span><span class="sxs-lookup"><span data-stu-id="4ba7a-122">ARSVault</span></span>
<span data-ttu-id="4ba7a-123">Параметр "хранилище" принимает значение типа "ARSVault" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4ba7a-123">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="4ba7a-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ba7a-124">OUTPUTS</span></span>

### <span data-ttu-id="4ba7a-125">Microsoft. Azure. Commands. RecoveryServices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="4ba7a-125">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="4ba7a-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ba7a-126">NOTES</span></span>

## <span data-ttu-id="4ba7a-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ba7a-127">RELATED LINKS</span></span>

[<span data-ttu-id="4ba7a-128">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4ba7a-128">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="4ba7a-129">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="4ba7a-129">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="4ba7a-130">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4ba7a-130">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)


