---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: dc1ea08b0770c7438574d4ef2cc6a97cb99f2909
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732995"
---
# <span data-ttu-id="e1c9f-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="e1c9f-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="e1c9f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e1c9f-102">SYNOPSIS</span></span>
<span data-ttu-id="e1c9f-103">Создает объект конфигурации для учетных данных хранилища ключей SQL Server на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e1c9f-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1c9f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e1c9f-104">SYNTAX</span></span>

```
New-AzureRmVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1c9f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1c9f-105">DESCRIPTION</span></span>

## <span data-ttu-id="e1c9f-106">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e1c9f-106">EXAMPLES</span></span>

## <span data-ttu-id="e1c9f-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e1c9f-107">PARAMETERS</span></span>

### <span data-ttu-id="e1c9f-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="e1c9f-108">-AzureKeyVaultUrl</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1c9f-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="e1c9f-109">-CredentialName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1c9f-110">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="e1c9f-110">-Enable</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1c9f-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1c9f-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="e1c9f-112">-Намерено</span><span class="sxs-lookup"><span data-stu-id="e1c9f-112">-ServicePrincipalName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1c9f-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="e1c9f-113">-ServicePrincipalSecret</span></span>
```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1c9f-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1c9f-114">-Confirm</span></span>
<span data-ttu-id="e1c9f-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e1c9f-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c9f-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1c9f-116">-WhatIf</span></span>
<span data-ttu-id="e1c9f-117">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e1c9f-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1c9f-118">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e1c9f-118">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c9f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1c9f-119">CommonParameters</span></span>
<span data-ttu-id="e1c9f-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e1c9f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1c9f-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1c9f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1c9f-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e1c9f-122">INPUTS</span></span>

### <span data-ttu-id="e1c9f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e1c9f-123">System.String</span></span>

### <span data-ttu-id="e1c9f-124">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e1c9f-124">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e1c9f-125">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="e1c9f-125">System.Security.SecureString</span></span>

## <span data-ttu-id="e1c9f-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1c9f-126">OUTPUTS</span></span>

### <span data-ttu-id="e1c9f-127">Microsoft. Azure. Commands. COMPUTE. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="e1c9f-127">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="e1c9f-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="e1c9f-128">NOTES</span></span>

## <span data-ttu-id="e1c9f-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1c9f-129">RELATED LINKS</span></span>
