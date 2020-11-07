---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 410cd159aacadd83ee03c6e628339be38ca42d8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904918"
---
# <span data-ttu-id="0bcd5-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="0bcd5-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="0bcd5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0bcd5-102">SYNOPSIS</span></span>
<span data-ttu-id="0bcd5-103">Получает свойства резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="0bcd5-103">Gets Backup properties.</span></span>

## <span data-ttu-id="0bcd5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0bcd5-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0bcd5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0bcd5-105">DESCRIPTION</span></span>
<span data-ttu-id="0bcd5-106">Командлет **Get-AzRecoveryServicesBackupProperty** получает свойства резервного копирования для хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="0bcd5-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="0bcd5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0bcd5-107">EXAMPLES</span></span>

### <span data-ttu-id="0bcd5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0bcd5-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="0bcd5-109">Получите свойство резервного хранилища для хранилища.</span><span class="sxs-lookup"><span data-stu-id="0bcd5-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="0bcd5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0bcd5-110">PARAMETERS</span></span>

### <span data-ttu-id="0bcd5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bcd5-111">-DefaultProfile</span></span>
<span data-ttu-id="0bcd5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0bcd5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bcd5-113">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="0bcd5-113">-Vault</span></span>
<span data-ttu-id="0bcd5-114">Указывает имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="0bcd5-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="0bcd5-115">Хранилище должно быть объектом **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="0bcd5-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="0bcd5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bcd5-116">CommonParameters</span></span>
<span data-ttu-id="0bcd5-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0bcd5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bcd5-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bcd5-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bcd5-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0bcd5-119">INPUTS</span></span>

### <span data-ttu-id="0bcd5-120">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="0bcd5-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="0bcd5-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0bcd5-121">OUTPUTS</span></span>

### <span data-ttu-id="0bcd5-122">Microsoft. Azure. Commands. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="0bcd5-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="0bcd5-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="0bcd5-123">NOTES</span></span>

## <span data-ttu-id="0bcd5-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0bcd5-124">RELATED LINKS</span></span>
