---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: de3604a4bf1f9c46bf88b2f3cda25982672e9096
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246020"
---
# <span data-ttu-id="c0767-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="c0767-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="c0767-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0767-102">SYNOPSIS</span></span>
<span data-ttu-id="c0767-103">Импортирует указанный файл параметров в хранилище ASR, чтобы задать контекст хранилища (контекст сеанса PowerShell) для последующих операций ASR в сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c0767-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

## <span data-ttu-id="c0767-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0767-104">SYNTAX</span></span>

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0767-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0767-105">DESCRIPTION</span></span>
<span data-ttu-id="c0767-106">Командлет **Import-AzRecoveryServicesAsrVaultSettingsFile** импортирует файл параметров хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="c0767-106">The **Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="c0767-107">Файл параметров хранилища используется для задания контекста хранилища для последующих операций восстановления сайта Azure в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="c0767-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="c0767-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0767-108">EXAMPLES</span></span>

### <span data-ttu-id="c0767-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c0767-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="c0767-110">Импортирует указанный файл параметров хранилища служб восстановления и возвращает параметры импортированного хранилища.</span><span class="sxs-lookup"><span data-stu-id="c0767-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="c0767-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0767-111">PARAMETERS</span></span>

### <span data-ttu-id="c0767-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0767-112">-DefaultProfile</span></span>
<span data-ttu-id="c0767-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0767-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c0767-114">-Path</span><span class="sxs-lookup"><span data-stu-id="c0767-114">-Path</span></span>
<span data-ttu-id="c0767-115">Указывает путь к папке для файла параметров в хранилище ASR.</span><span class="sxs-lookup"><span data-stu-id="c0767-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="c0767-116">Этот файл можно скачать с портала хранилища служб восстановления и сохранить на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="c0767-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0767-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0767-117">-Confirm</span></span>
<span data-ttu-id="c0767-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c0767-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0767-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0767-119">-WhatIf</span></span>
<span data-ttu-id="c0767-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c0767-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0767-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c0767-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0767-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0767-122">CommonParameters</span></span>
<span data-ttu-id="c0767-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0767-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0767-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0767-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0767-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0767-125">INPUTS</span></span>

### <span data-ttu-id="c0767-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c0767-126">System.String</span></span>

## <span data-ttu-id="c0767-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0767-127">OUTPUTS</span></span>

### <span data-ttu-id="c0767-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="c0767-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="c0767-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0767-129">NOTES</span></span>

## <span data-ttu-id="c0767-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0767-130">RELATED LINKS</span></span>

[<span data-ttu-id="c0767-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="c0767-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzRecoveryServicesAsrVaultSettingsFile.md)