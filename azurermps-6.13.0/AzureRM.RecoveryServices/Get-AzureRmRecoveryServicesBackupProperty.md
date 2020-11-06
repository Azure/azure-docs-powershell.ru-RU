---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: d900da862572c0e3a51f288a7e6bec948f7aeba4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562732"
---
# <span data-ttu-id="7325b-101">Get-AzureRmRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="7325b-101">Get-AzureRmRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="7325b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7325b-102">SYNOPSIS</span></span>
<span data-ttu-id="7325b-103">Получает свойства резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="7325b-103">Gets Backup properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7325b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7325b-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7325b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7325b-105">DESCRIPTION</span></span>
<span data-ttu-id="7325b-106">Командлет **Get-AzureRmRecoveryServicesBackupProperty** получает свойства резервного копирования для хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="7325b-106">The **Get-AzureRmRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="7325b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7325b-107">EXAMPLES</span></span>

### <span data-ttu-id="7325b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7325b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="7325b-109">Получите свойство резервного хранилища для хранилища.</span><span class="sxs-lookup"><span data-stu-id="7325b-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="7325b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7325b-110">PARAMETERS</span></span>

### <span data-ttu-id="7325b-111">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="7325b-111">-Vault</span></span>
<span data-ttu-id="7325b-112">Указывает имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="7325b-112">Specifies the name of the vault.</span></span>
<span data-ttu-id="7325b-113">Хранилище должно быть объектом **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="7325b-113">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="7325b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7325b-114">-DefaultProfile</span></span>
<span data-ttu-id="7325b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7325b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7325b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7325b-116">CommonParameters</span></span>
<span data-ttu-id="7325b-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7325b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7325b-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7325b-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7325b-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7325b-119">INPUTS</span></span>

### <span data-ttu-id="7325b-120">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="7325b-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="7325b-121">Параметры: хранилище (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7325b-121">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="7325b-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7325b-122">OUTPUTS</span></span>

### <span data-ttu-id="7325b-123">Microsoft. Azure. Commands. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="7325b-123">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="7325b-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="7325b-124">NOTES</span></span>

## <span data-ttu-id="7325b-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7325b-125">RELATED LINKS</span></span>
