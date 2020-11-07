---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: ad22cbe1cb17e69358ef386b478fe929abe415b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732425"
---
# <span data-ttu-id="d45b7-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="d45b7-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="d45b7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d45b7-102">SYNOPSIS</span></span>
<span data-ttu-id="d45b7-103">Импортирует указанный файл параметров в хранилище ASR, чтобы задать контекст хранилища (контекст сеанса PowerShell) для последующих операций ASR в сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d45b7-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d45b7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d45b7-104">SYNTAX</span></span>

```
Import-AzureRmRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d45b7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d45b7-105">DESCRIPTION</span></span>
<span data-ttu-id="d45b7-106">Командлет **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** импортирует файл параметров хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d45b7-106">The **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="d45b7-107">Файл параметров хранилища используется для задания контекста хранилища для последующих операций восстановления сайта Azure в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="d45b7-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="d45b7-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d45b7-108">EXAMPLES</span></span>

### <span data-ttu-id="d45b7-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d45b7-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzureRmRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="d45b7-110">Импортирует указанный файл параметров хранилища служб восстановления и возвращает параметры импортированного хранилища.</span><span class="sxs-lookup"><span data-stu-id="d45b7-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="d45b7-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d45b7-111">PARAMETERS</span></span>

### <span data-ttu-id="d45b7-112">-Path</span><span class="sxs-lookup"><span data-stu-id="d45b7-112">-Path</span></span>
<span data-ttu-id="d45b7-113">Задает путь к файлу параметров для хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="d45b7-113">Specifies the path of the ASR vault settings file.</span></span>
<span data-ttu-id="d45b7-114">Этот файл можно скачать с портала хранилища служб восстановления и сохранить на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="d45b7-114">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d45b7-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d45b7-115">-Confirm</span></span>
<span data-ttu-id="d45b7-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d45b7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d45b7-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d45b7-117">-WhatIf</span></span>
<span data-ttu-id="d45b7-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d45b7-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d45b7-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d45b7-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d45b7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d45b7-120">CommonParameters</span></span>
<span data-ttu-id="d45b7-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d45b7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d45b7-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d45b7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d45b7-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d45b7-123">INPUTS</span></span>

### <span data-ttu-id="d45b7-124">System. String</span><span class="sxs-lookup"><span data-stu-id="d45b7-124">System.String</span></span>

## <span data-ttu-id="d45b7-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d45b7-125">OUTPUTS</span></span>

### <span data-ttu-id="d45b7-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="d45b7-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="d45b7-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="d45b7-127">NOTES</span></span>

## <span data-ttu-id="d45b7-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d45b7-128">RELATED LINKS</span></span>

[<span data-ttu-id="d45b7-129">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="d45b7-129">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesAsrVaultSettingsFile.md)
