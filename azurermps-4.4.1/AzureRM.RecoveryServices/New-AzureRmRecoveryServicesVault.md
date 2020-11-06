---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: d9163e42b199dd5178e37a7d1bbe22abbb05c7f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559576"
---
# <span data-ttu-id="b2aec-101">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b2aec-101">New-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="b2aec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b2aec-102">SYNOPSIS</span></span>
<span data-ttu-id="b2aec-103">Создание нового хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="b2aec-103">Creates a new Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2aec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b2aec-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2aec-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2aec-105">DESCRIPTION</span></span>
<span data-ttu-id="b2aec-106">Командлет **New-AzureRmRecoveryServicesVault** создает новое хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="b2aec-106">The **New-AzureRmRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="b2aec-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b2aec-107">EXAMPLES</span></span>

## <span data-ttu-id="b2aec-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b2aec-108">PARAMETERS</span></span>

### <span data-ttu-id="b2aec-109">-Location</span><span class="sxs-lookup"><span data-stu-id="b2aec-109">-Location</span></span>
<span data-ttu-id="b2aec-110">Указывает название географического расположения хранилища.</span><span class="sxs-lookup"><span data-stu-id="b2aec-110">Specifies the name of the geographic location of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2aec-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b2aec-111">-Name</span></span>
<span data-ttu-id="b2aec-112">Указывает имя создаваемого хранилища.</span><span class="sxs-lookup"><span data-stu-id="b2aec-112">Specifies the name of the vault to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2aec-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2aec-113">-ResourceGroupName</span></span>
<span data-ttu-id="b2aec-114">Указывает имя группы ресурсов Azure, в которой нужно создать или из которой нужно получить указанный объект служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="b2aec-114">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2aec-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2aec-115">-Confirm</span></span>
<span data-ttu-id="b2aec-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b2aec-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2aec-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2aec-117">-WhatIf</span></span>
<span data-ttu-id="b2aec-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b2aec-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2aec-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b2aec-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2aec-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2aec-120">-DefaultProfile</span></span>
<span data-ttu-id="b2aec-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2aec-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2aec-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2aec-122">CommonParameters</span></span>
<span data-ttu-id="b2aec-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b2aec-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2aec-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2aec-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2aec-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b2aec-125">INPUTS</span></span>

## <span data-ttu-id="b2aec-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2aec-126">OUTPUTS</span></span>

### <span data-ttu-id="b2aec-127">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="b2aec-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="b2aec-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="b2aec-128">NOTES</span></span>

## <span data-ttu-id="b2aec-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2aec-129">RELATED LINKS</span></span>

[<span data-ttu-id="b2aec-130">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b2aec-130">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="b2aec-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="b2aec-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="b2aec-132">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b2aec-132">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


