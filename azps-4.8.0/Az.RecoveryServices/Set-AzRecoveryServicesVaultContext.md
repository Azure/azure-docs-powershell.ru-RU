---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 48454b3b6bda283763b05657b0bc652fa9973233
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244016"
---
# <span data-ttu-id="94cb3-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="94cb3-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="94cb3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94cb3-102">SYNOPSIS</span></span>

<span data-ttu-id="94cb3-103">Задает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="94cb3-103">Sets vault context.</span></span>

## <span data-ttu-id="94cb3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94cb3-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94cb3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94cb3-105">DESCRIPTION</span></span>

<span data-ttu-id="94cb3-106">Командлет **Set-AzRecoveryServicesVaultContext** задает контекст хранилища для служб Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="94cb3-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="94cb3-107">Предупреждение: Этот командлет не рекомендуется использовать в будущих версиях исправлений.</span><span class="sxs-lookup"><span data-stu-id="94cb3-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="94cb3-108">Для него не будет использоваться замена.</span><span class="sxs-lookup"><span data-stu-id="94cb3-108">There will be no replacement for it.</span></span> <span data-ttu-id="94cb3-109">Используйте параметр-VaultId во всех командах служб восстановления, пересылаемых вперед.</span><span class="sxs-lookup"><span data-stu-id="94cb3-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="94cb3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94cb3-110">EXAMPLES</span></span>

### <span data-ttu-id="94cb3-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="94cb3-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="94cb3-112">Задает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="94cb3-112">Sets vault context.</span></span>

## <span data-ttu-id="94cb3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94cb3-113">PARAMETERS</span></span>

### <span data-ttu-id="94cb3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94cb3-114">-DefaultProfile</span></span>

<span data-ttu-id="94cb3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94cb3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94cb3-116">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="94cb3-116">-Vault</span></span>

<span data-ttu-id="94cb3-117">Указывает имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="94cb3-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="94cb3-118">Хранилище должно быть объектом **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="94cb3-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="94cb3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94cb3-119">CommonParameters</span></span>
<span data-ttu-id="94cb3-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94cb3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94cb3-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94cb3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94cb3-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94cb3-122">INPUTS</span></span>

### <span data-ttu-id="94cb3-123">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="94cb3-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="94cb3-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94cb3-124">OUTPUTS</span></span>

### <span data-ttu-id="94cb3-125">System. void</span><span class="sxs-lookup"><span data-stu-id="94cb3-125">System.Void</span></span>

## <span data-ttu-id="94cb3-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="94cb3-126">NOTES</span></span>

## <span data-ttu-id="94cb3-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94cb3-127">RELATED LINKS</span></span>