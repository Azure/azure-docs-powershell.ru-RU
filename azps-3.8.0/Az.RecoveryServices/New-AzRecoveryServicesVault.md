---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
ms.openlocfilehash: 3bb602d148b0843def129a1e4538d9ef8fdbe169
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072683"
---
# <span data-ttu-id="f46cf-101">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f46cf-101">New-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="f46cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f46cf-102">SYNOPSIS</span></span>
<span data-ttu-id="f46cf-103">Создание нового хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="f46cf-103">Creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="f46cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f46cf-104">SYNTAX</span></span>

```
New-AzRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f46cf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f46cf-105">DESCRIPTION</span></span>
<span data-ttu-id="f46cf-106">Командлет **New-AzRecoveryServicesVault** создает новое хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="f46cf-106">The **New-AzRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="f46cf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f46cf-107">EXAMPLES</span></span>

### <span data-ttu-id="f46cf-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f46cf-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="f46cf-109">Создание хранилища службы восстановления в группе ресурсов и указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="f46cf-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="f46cf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f46cf-110">PARAMETERS</span></span>

### <span data-ttu-id="f46cf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f46cf-111">-DefaultProfile</span></span>
<span data-ttu-id="f46cf-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f46cf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f46cf-113">-Location</span><span class="sxs-lookup"><span data-stu-id="f46cf-113">-Location</span></span>
<span data-ttu-id="f46cf-114">Указывает название географического расположения хранилища.</span><span class="sxs-lookup"><span data-stu-id="f46cf-114">Specifies the name of the geographic location of the vault.</span></span>

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

### <span data-ttu-id="f46cf-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f46cf-115">-Name</span></span>
<span data-ttu-id="f46cf-116">Указывает имя создаваемого хранилища.</span><span class="sxs-lookup"><span data-stu-id="f46cf-116">Specifies the name of the vault to create.</span></span>

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

### <span data-ttu-id="f46cf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f46cf-117">-ResourceGroupName</span></span>
<span data-ttu-id="f46cf-118">Указывает имя группы ресурсов Azure, в которой нужно создать или из которой нужно получить указанный объект служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="f46cf-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="f46cf-119">-Тег</span><span class="sxs-lookup"><span data-stu-id="f46cf-119">-Tag</span></span>

<span data-ttu-id="f46cf-120">Указывает теги, которые нужно добавить в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="f46cf-120">Specifies the Tags to add to the Recovery Services Vault</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f46cf-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f46cf-121">-Confirm</span></span>
<span data-ttu-id="f46cf-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f46cf-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f46cf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f46cf-123">-WhatIf</span></span>
<span data-ttu-id="f46cf-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f46cf-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f46cf-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f46cf-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f46cf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f46cf-126">CommonParameters</span></span>
<span data-ttu-id="f46cf-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f46cf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f46cf-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f46cf-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f46cf-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f46cf-129">INPUTS</span></span>

### <span data-ttu-id="f46cf-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="f46cf-130">None</span></span>

## <span data-ttu-id="f46cf-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f46cf-131">OUTPUTS</span></span>

### <span data-ttu-id="f46cf-132">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="f46cf-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="f46cf-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="f46cf-133">NOTES</span></span>

## <span data-ttu-id="f46cf-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f46cf-134">RELATED LINKS</span></span>

[<span data-ttu-id="f46cf-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f46cf-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="f46cf-136">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f46cf-136">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="f46cf-137">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f46cf-137">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


