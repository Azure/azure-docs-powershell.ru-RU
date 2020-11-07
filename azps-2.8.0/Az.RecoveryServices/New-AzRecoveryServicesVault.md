---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
ms.openlocfilehash: 65694116a924759c4cf29a7abcf95da7a03df39f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905866"
---
# <span data-ttu-id="924a4-101">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="924a4-101">New-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="924a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="924a4-102">SYNOPSIS</span></span>
<span data-ttu-id="924a4-103">Создание нового хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="924a4-103">Creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="924a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="924a4-104">SYNTAX</span></span>

```
New-AzRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="924a4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="924a4-105">DESCRIPTION</span></span>
<span data-ttu-id="924a4-106">Командлет **New-AzRecoveryServicesVault** создает новое хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="924a4-106">The **New-AzRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="924a4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="924a4-107">EXAMPLES</span></span>

### <span data-ttu-id="924a4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="924a4-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="924a4-109">Создание хранилища службы восстановления в группе ресурсов и указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="924a4-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="924a4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="924a4-110">PARAMETERS</span></span>

### <span data-ttu-id="924a4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="924a4-111">-DefaultProfile</span></span>
<span data-ttu-id="924a4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="924a4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="924a4-113">-Location</span><span class="sxs-lookup"><span data-stu-id="924a4-113">-Location</span></span>
<span data-ttu-id="924a4-114">Указывает название географического расположения хранилища.</span><span class="sxs-lookup"><span data-stu-id="924a4-114">Specifies the name of the geographic location of the vault.</span></span>

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

### <span data-ttu-id="924a4-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="924a4-115">-Name</span></span>
<span data-ttu-id="924a4-116">Указывает имя создаваемого хранилища.</span><span class="sxs-lookup"><span data-stu-id="924a4-116">Specifies the name of the vault to create.</span></span>

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

### <span data-ttu-id="924a4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="924a4-117">-ResourceGroupName</span></span>
<span data-ttu-id="924a4-118">Указывает имя группы ресурсов Azure, в которой нужно создать или из которой нужно получить указанный объект служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="924a4-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="924a4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="924a4-119">-Confirm</span></span>
<span data-ttu-id="924a4-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="924a4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="924a4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="924a4-121">-WhatIf</span></span>
<span data-ttu-id="924a4-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="924a4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="924a4-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="924a4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="924a4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="924a4-124">CommonParameters</span></span>
<span data-ttu-id="924a4-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="924a4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="924a4-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="924a4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="924a4-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="924a4-127">INPUTS</span></span>

### <span data-ttu-id="924a4-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="924a4-128">None</span></span>

## <span data-ttu-id="924a4-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="924a4-129">OUTPUTS</span></span>

### <span data-ttu-id="924a4-130">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="924a4-130">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="924a4-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="924a4-131">NOTES</span></span>

## <span data-ttu-id="924a4-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="924a4-132">RELATED LINKS</span></span>

[<span data-ttu-id="924a4-133">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="924a4-133">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="924a4-134">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="924a4-134">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="924a4-135">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="924a4-135">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


