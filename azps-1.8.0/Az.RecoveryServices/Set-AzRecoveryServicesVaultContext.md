---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 4d8839d36bf337e3a710fe31384bb022582a371d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729604"
---
# <span data-ttu-id="d1fb0-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="d1fb0-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="d1fb0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d1fb0-102">SYNOPSIS</span></span>
<span data-ttu-id="d1fb0-103">Задает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-103">Sets vault context.</span></span>

## <span data-ttu-id="d1fb0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d1fb0-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1fb0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1fb0-105">DESCRIPTION</span></span>
<span data-ttu-id="d1fb0-106">Командлет **Set-AzRecoveryServicesVaultContext** задает контекст хранилища для служб Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="d1fb0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d1fb0-107">EXAMPLES</span></span>

### <span data-ttu-id="d1fb0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d1fb0-108">Example 1</span></span>
```
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="d1fb0-109">Задает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-109">Sets vault context.</span></span>

## <span data-ttu-id="d1fb0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d1fb0-110">PARAMETERS</span></span>

### <span data-ttu-id="d1fb0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1fb0-111">-DefaultProfile</span></span>
<span data-ttu-id="d1fb0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1fb0-113">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="d1fb0-113">-Vault</span></span>
<span data-ttu-id="d1fb0-114">Указывает имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="d1fb0-115">Хранилище должно быть объектом **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="d1fb0-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="d1fb0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1fb0-116">CommonParameters</span></span>
<span data-ttu-id="d1fb0-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1fb0-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1fb0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1fb0-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d1fb0-119">INPUTS</span></span>

### <span data-ttu-id="d1fb0-120">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="d1fb0-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="d1fb0-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1fb0-121">OUTPUTS</span></span>

### <span data-ttu-id="d1fb0-122">System. void</span><span class="sxs-lookup"><span data-stu-id="d1fb0-122">System.Void</span></span>

## <span data-ttu-id="d1fb0-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="d1fb0-123">NOTES</span></span>

## <span data-ttu-id="d1fb0-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1fb0-124">RELATED LINKS</span></span>