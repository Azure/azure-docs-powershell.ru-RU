---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
ms.openlocfilehash: 811ac8b9f8922844dd5153a4fa02abc4c023f7a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953304"
---
# <span data-ttu-id="4586a-101">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4586a-101">New-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="4586a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4586a-102">SYNOPSIS</span></span>
<span data-ttu-id="4586a-103">Создание нового хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="4586a-103">Creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="4586a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4586a-104">SYNTAX</span></span>

```
New-AzRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4586a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4586a-105">DESCRIPTION</span></span>
<span data-ttu-id="4586a-106">Для создания нового хранилища служб восстановления создается новый **cmdlet New-AzRecoveryServicesVault.**</span><span class="sxs-lookup"><span data-stu-id="4586a-106">The **New-AzRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="4586a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4586a-107">EXAMPLES</span></span>

### <span data-ttu-id="4586a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4586a-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="4586a-109">Создайте хранилище службы восстановления в группе ресурсов и заданном расположении.</span><span class="sxs-lookup"><span data-stu-id="4586a-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="4586a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4586a-110">PARAMETERS</span></span>

### <span data-ttu-id="4586a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4586a-111">-DefaultProfile</span></span>
<span data-ttu-id="4586a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4586a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4586a-113">-Location</span><span class="sxs-lookup"><span data-stu-id="4586a-113">-Location</span></span>
<span data-ttu-id="4586a-114">Указывает имя географического расположения сейфа.</span><span class="sxs-lookup"><span data-stu-id="4586a-114">Specifies the name of the geographic location of the vault.</span></span>

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

### <span data-ttu-id="4586a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4586a-115">-Name</span></span>
<span data-ttu-id="4586a-116">Указывает имя создаемого сейфа.</span><span class="sxs-lookup"><span data-stu-id="4586a-116">Specifies the name of the vault to create.</span></span>

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

### <span data-ttu-id="4586a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4586a-117">-ResourceGroupName</span></span>
<span data-ttu-id="4586a-118">Имя группы ресурсов Azure, в которой нужно создать или из которой получить указанный объект служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="4586a-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="4586a-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="4586a-119">-Tag</span></span>

<span data-ttu-id="4586a-120">Определяет теги, которые нужно добавить в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="4586a-120">Specifies the Tags to add to the Recovery Services Vault</span></span>

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

### <span data-ttu-id="4586a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4586a-121">-Confirm</span></span>
<span data-ttu-id="4586a-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4586a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4586a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4586a-123">-WhatIf</span></span>
<span data-ttu-id="4586a-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4586a-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4586a-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4586a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4586a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4586a-126">CommonParameters</span></span>
<span data-ttu-id="4586a-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4586a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4586a-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4586a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4586a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4586a-129">INPUTS</span></span>

### <span data-ttu-id="4586a-130">Нет</span><span class="sxs-lookup"><span data-stu-id="4586a-130">None</span></span>

## <span data-ttu-id="4586a-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4586a-131">OUTPUTS</span></span>

### <span data-ttu-id="4586a-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="4586a-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="4586a-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4586a-133">NOTES</span></span>

## <span data-ttu-id="4586a-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4586a-134">RELATED LINKS</span></span>

[<span data-ttu-id="4586a-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4586a-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="4586a-136">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="4586a-136">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="4586a-137">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4586a-137">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


