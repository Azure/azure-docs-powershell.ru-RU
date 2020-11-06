---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/set-azurermrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
ms.openlocfilehash: 0989bdcc14a9f7e3cbd65af11aea843cdd0ec6e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558331"
---
# <span data-ttu-id="c7355-101">Set-AzureRmRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="c7355-101">Set-AzureRmRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="c7355-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7355-102">SYNOPSIS</span></span>
<span data-ttu-id="c7355-103">Задает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="c7355-103">Sets vault context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7355-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7355-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7355-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7355-105">DESCRIPTION</span></span>
<span data-ttu-id="c7355-106">Командлет **Set-AzureRmRecoveryServicesVaultContext** задает контекст хранилища для служб Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="c7355-106">The **Set-AzureRmRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="c7355-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7355-107">EXAMPLES</span></span>

### <span data-ttu-id="c7355-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c7355-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="c7355-109">Задает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="c7355-109">Sets vault context.</span></span>

## <span data-ttu-id="c7355-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7355-110">PARAMETERS</span></span>

### <span data-ttu-id="c7355-111">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="c7355-111">-Vault</span></span>
<span data-ttu-id="c7355-112">Указывает имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="c7355-112">Specifies the name of the vault.</span></span>
<span data-ttu-id="c7355-113">Хранилище должно быть объектом **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="c7355-113">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="c7355-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7355-114">-DefaultProfile</span></span>
<span data-ttu-id="c7355-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7355-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7355-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7355-116">CommonParameters</span></span>
<span data-ttu-id="c7355-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7355-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7355-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7355-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7355-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7355-119">INPUTS</span></span>

### <span data-ttu-id="c7355-120">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="c7355-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="c7355-121">Параметры: хранилище (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c7355-121">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="c7355-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7355-122">OUTPUTS</span></span>

### <span data-ttu-id="c7355-123">System. void</span><span class="sxs-lookup"><span data-stu-id="c7355-123">System.Void</span></span>

## <span data-ttu-id="c7355-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7355-124">NOTES</span></span>

## <span data-ttu-id="c7355-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7355-125">RELATED LINKS</span></span>
