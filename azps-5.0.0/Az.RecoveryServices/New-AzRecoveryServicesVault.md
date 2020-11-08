---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
ms.openlocfilehash: 3bb602d148b0843def129a1e4538d9ef8fdbe169
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248051"
---
# <span data-ttu-id="41cd3-101">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="41cd3-101">New-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="41cd3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="41cd3-103">Создание нового хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="41cd3-103">Creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="41cd3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41cd3-104">SYNTAX</span></span>

```
New-AzRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41cd3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41cd3-105">DESCRIPTION</span></span>
<span data-ttu-id="41cd3-106">Командлет **New-AzRecoveryServicesVault** создает новое хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="41cd3-106">The **New-AzRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="41cd3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41cd3-107">EXAMPLES</span></span>

### <span data-ttu-id="41cd3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="41cd3-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="41cd3-109">Создание хранилища службы восстановления в группе ресурсов и указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="41cd3-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="41cd3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41cd3-110">PARAMETERS</span></span>

### <span data-ttu-id="41cd3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41cd3-111">-DefaultProfile</span></span>
<span data-ttu-id="41cd3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41cd3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41cd3-113">-Location</span><span class="sxs-lookup"><span data-stu-id="41cd3-113">-Location</span></span>
<span data-ttu-id="41cd3-114">Указывает название географического расположения хранилища.</span><span class="sxs-lookup"><span data-stu-id="41cd3-114">Specifies the name of the geographic location of the vault.</span></span>

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

### <span data-ttu-id="41cd3-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="41cd3-115">-Name</span></span>
<span data-ttu-id="41cd3-116">Указывает имя создаваемого хранилища.</span><span class="sxs-lookup"><span data-stu-id="41cd3-116">Specifies the name of the vault to create.</span></span>

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

### <span data-ttu-id="41cd3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41cd3-117">-ResourceGroupName</span></span>
<span data-ttu-id="41cd3-118">Указывает имя группы ресурсов Azure, в которой нужно создать или из которой нужно получить указанный объект служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="41cd3-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="41cd3-119">-Тег</span><span class="sxs-lookup"><span data-stu-id="41cd3-119">-Tag</span></span>

<span data-ttu-id="41cd3-120">Указывает теги, которые нужно добавить в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="41cd3-120">Specifies the Tags to add to the Recovery Services Vault</span></span>

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

### <span data-ttu-id="41cd3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41cd3-121">-Confirm</span></span>
<span data-ttu-id="41cd3-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="41cd3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41cd3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41cd3-123">-WhatIf</span></span>
<span data-ttu-id="41cd3-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="41cd3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41cd3-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="41cd3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41cd3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41cd3-126">CommonParameters</span></span>
<span data-ttu-id="41cd3-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41cd3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41cd3-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41cd3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41cd3-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41cd3-129">INPUTS</span></span>

### <span data-ttu-id="41cd3-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="41cd3-130">None</span></span>

## <span data-ttu-id="41cd3-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41cd3-131">OUTPUTS</span></span>

### <span data-ttu-id="41cd3-132">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="41cd3-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="41cd3-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="41cd3-133">NOTES</span></span>

## <span data-ttu-id="41cd3-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41cd3-134">RELATED LINKS</span></span>

[<span data-ttu-id="41cd3-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="41cd3-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="41cd3-136">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="41cd3-136">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="41cd3-137">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="41cd3-137">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


