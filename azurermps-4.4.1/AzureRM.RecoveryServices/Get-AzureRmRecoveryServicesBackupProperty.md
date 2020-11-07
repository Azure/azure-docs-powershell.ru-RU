---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: 3e93df0adfe1e1bc10d5ea74dd189bee60595824
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733642"
---
# <span data-ttu-id="7f383-101">Get-AzureRmRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="7f383-101">Get-AzureRmRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="7f383-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7f383-102">SYNOPSIS</span></span>
<span data-ttu-id="7f383-103">Получает свойства резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="7f383-103">Gets Backup properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f383-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7f383-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f383-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f383-105">DESCRIPTION</span></span>
<span data-ttu-id="7f383-106">Командлет **Get-AzureRmRecoveryServicesBackupProperty** получает свойства резервного копирования для хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="7f383-106">The **Get-AzureRmRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="7f383-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7f383-107">EXAMPLES</span></span>

## <span data-ttu-id="7f383-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7f383-108">PARAMETERS</span></span>

### <span data-ttu-id="7f383-109">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="7f383-109">-Vault</span></span>
<span data-ttu-id="7f383-110">Указывает имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="7f383-110">Specifies the name of the vault.</span></span>
<span data-ttu-id="7f383-111">Хранилище должно быть объектом **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="7f383-111">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="7f383-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f383-112">-DefaultProfile</span></span>
<span data-ttu-id="7f383-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f383-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f383-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f383-114">CommonParameters</span></span>
<span data-ttu-id="7f383-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7f383-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f383-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f383-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f383-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7f383-117">INPUTS</span></span>

### <span data-ttu-id="7f383-118">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="7f383-118">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="7f383-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f383-119">OUTPUTS</span></span>

### <span data-ttu-id="7f383-120">Microsoft. Azure. Commands. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="7f383-120">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="7f383-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="7f383-121">NOTES</span></span>

## <span data-ttu-id="7f383-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f383-122">RELATED LINKS</span></span>

