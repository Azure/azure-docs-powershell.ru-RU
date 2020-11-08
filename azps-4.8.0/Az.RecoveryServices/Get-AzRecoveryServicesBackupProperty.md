---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: efe463bab4195dfb09692f76d0e02e3aeaa59344
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079375"
---
# <span data-ttu-id="d485f-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="d485f-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="d485f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d485f-102">SYNOPSIS</span></span>
<span data-ttu-id="d485f-103">Получает свойства резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="d485f-103">Gets Backup properties.</span></span>

## <span data-ttu-id="d485f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d485f-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d485f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d485f-105">DESCRIPTION</span></span>
<span data-ttu-id="d485f-106">Командлет **Get-AzRecoveryServicesBackupProperty** получает свойства резервного копирования для хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="d485f-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="d485f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d485f-107">EXAMPLES</span></span>

### <span data-ttu-id="d485f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d485f-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="d485f-109">Получите свойство резервного хранилища для хранилища.</span><span class="sxs-lookup"><span data-stu-id="d485f-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="d485f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d485f-110">PARAMETERS</span></span>

### <span data-ttu-id="d485f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d485f-111">-DefaultProfile</span></span>
<span data-ttu-id="d485f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d485f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d485f-113">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="d485f-113">-Vault</span></span>
<span data-ttu-id="d485f-114">Указывает имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="d485f-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="d485f-115">Хранилище должно быть объектом **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="d485f-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="d485f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d485f-116">CommonParameters</span></span>
<span data-ttu-id="d485f-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d485f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d485f-118">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d485f-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d485f-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d485f-119">INPUTS</span></span>

### <span data-ttu-id="d485f-120">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="d485f-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="d485f-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d485f-121">OUTPUTS</span></span>

### <span data-ttu-id="d485f-122">Microsoft. Azure. Commands. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="d485f-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="d485f-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="d485f-123">NOTES</span></span>

## <span data-ttu-id="d485f-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d485f-124">RELATED LINKS</span></span>