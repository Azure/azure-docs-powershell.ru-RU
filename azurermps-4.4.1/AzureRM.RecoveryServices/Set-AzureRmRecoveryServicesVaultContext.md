---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
ms.openlocfilehash: d8743b12757d5845107d6a38689059b90bf1e287
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734250"
---
# <span data-ttu-id="b43a1-101">Set-AzureRmRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="b43a1-101">Set-AzureRmRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="b43a1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b43a1-102">SYNOPSIS</span></span>
<span data-ttu-id="b43a1-103">Задает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="b43a1-103">Sets vault context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b43a1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b43a1-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b43a1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b43a1-105">DESCRIPTION</span></span>
<span data-ttu-id="b43a1-106">Командлет **Set-AzureRmRecoveryServicesVaultContext** задает контекст хранилища для служб Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b43a1-106">The **Set-AzureRmRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="b43a1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b43a1-107">EXAMPLES</span></span>

## <span data-ttu-id="b43a1-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b43a1-108">PARAMETERS</span></span>

### <span data-ttu-id="b43a1-109">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="b43a1-109">-Vault</span></span>
<span data-ttu-id="b43a1-110">Указывает имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="b43a1-110">Specifies the name of the vault.</span></span>
<span data-ttu-id="b43a1-111">Хранилище должно быть объектом **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="b43a1-111">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="b43a1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b43a1-112">-DefaultProfile</span></span>
<span data-ttu-id="b43a1-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b43a1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b43a1-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b43a1-114">CommonParameters</span></span>
<span data-ttu-id="b43a1-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b43a1-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b43a1-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b43a1-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b43a1-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b43a1-117">INPUTS</span></span>

### <span data-ttu-id="b43a1-118">ARSVault</span><span class="sxs-lookup"><span data-stu-id="b43a1-118">ARSVault</span></span>
<span data-ttu-id="b43a1-119">Параметр "хранилище" принимает значение типа "ARSVault" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b43a1-119">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="b43a1-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b43a1-120">OUTPUTS</span></span>

## <span data-ttu-id="b43a1-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="b43a1-121">NOTES</span></span>

## <span data-ttu-id="b43a1-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b43a1-122">RELATED LINKS</span></span>

