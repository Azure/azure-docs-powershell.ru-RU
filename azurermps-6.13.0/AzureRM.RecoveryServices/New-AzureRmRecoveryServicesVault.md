---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/new-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 08166ea1ebe4c78521a68f9e5423a7947e78b699
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568420"
---
# <span data-ttu-id="511f2-101">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="511f2-101">New-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="511f2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="511f2-102">SYNOPSIS</span></span>
<span data-ttu-id="511f2-103">Создание нового хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="511f2-103">Creates a new Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="511f2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="511f2-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="511f2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="511f2-105">DESCRIPTION</span></span>
<span data-ttu-id="511f2-106">Командлет **New-AzureRmRecoveryServicesVault** создает новое хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="511f2-106">The **New-AzureRmRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="511f2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="511f2-107">EXAMPLES</span></span>

### <span data-ttu-id="511f2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="511f2-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="511f2-109">Создание хранилища службы восстановления в группе ресурсов и указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="511f2-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="511f2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="511f2-110">PARAMETERS</span></span>

### <span data-ttu-id="511f2-111">-Location</span><span class="sxs-lookup"><span data-stu-id="511f2-111">-Location</span></span>
<span data-ttu-id="511f2-112">Указывает название географического расположения хранилища.</span><span class="sxs-lookup"><span data-stu-id="511f2-112">Specifies the name of the geographic location of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="511f2-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="511f2-113">-Name</span></span>
<span data-ttu-id="511f2-114">Указывает имя создаваемого хранилища.</span><span class="sxs-lookup"><span data-stu-id="511f2-114">Specifies the name of the vault to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="511f2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="511f2-115">-ResourceGroupName</span></span>
<span data-ttu-id="511f2-116">Указывает имя группы ресурсов Azure, в которой нужно создать или из которой нужно получить указанный объект служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="511f2-116">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="511f2-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="511f2-117">-Confirm</span></span>
<span data-ttu-id="511f2-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="511f2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="511f2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="511f2-119">-WhatIf</span></span>
<span data-ttu-id="511f2-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="511f2-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="511f2-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="511f2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="511f2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="511f2-122">-DefaultProfile</span></span>
<span data-ttu-id="511f2-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="511f2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="511f2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="511f2-124">CommonParameters</span></span>
<span data-ttu-id="511f2-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="511f2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="511f2-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="511f2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="511f2-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="511f2-127">INPUTS</span></span>

### <span data-ttu-id="511f2-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="511f2-128">None</span></span>

## <span data-ttu-id="511f2-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="511f2-129">OUTPUTS</span></span>

### <span data-ttu-id="511f2-130">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="511f2-130">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="511f2-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="511f2-131">NOTES</span></span>

## <span data-ttu-id="511f2-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="511f2-132">RELATED LINKS</span></span>

[<span data-ttu-id="511f2-133">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="511f2-133">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="511f2-134">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="511f2-134">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="511f2-135">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="511f2-135">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


