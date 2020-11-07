---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
ms.openlocfilehash: ee627065d1d6be8037d1a9b054ec6452b9becb41
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914586"
---
# <span data-ttu-id="77555-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="77555-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="77555-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77555-102">SYNOPSIS</span></span>
<span data-ttu-id="77555-103">Создает объект конфигурации для учетных данных хранилища ключей SQL Server на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="77555-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77555-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77555-104">SYNTAX</span></span>

```
New-AzureRmVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77555-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77555-105">DESCRIPTION</span></span>

## <span data-ttu-id="77555-106">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77555-106">EXAMPLES</span></span>

## <span data-ttu-id="77555-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77555-107">PARAMETERS</span></span>

### <span data-ttu-id="77555-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="77555-108">-AzureKeyVaultUrl</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77555-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="77555-109">-CredentialName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77555-110">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="77555-110">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77555-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77555-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="77555-112">-Намерено</span><span class="sxs-lookup"><span data-stu-id="77555-112">-ServicePrincipalName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77555-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="77555-113">-ServicePrincipalSecret</span></span>
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77555-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77555-114">-Confirm</span></span>
<span data-ttu-id="77555-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="77555-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77555-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77555-116">-WhatIf</span></span>
<span data-ttu-id="77555-117">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="77555-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="77555-118">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="77555-118">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77555-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77555-119">CommonParameters</span></span>
<span data-ttu-id="77555-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77555-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77555-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77555-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77555-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77555-122">INPUTS</span></span>

### <span data-ttu-id="77555-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="77555-123">None</span></span>
<span data-ttu-id="77555-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="77555-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="77555-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77555-125">OUTPUTS</span></span>

### <span data-ttu-id="77555-126">Microsoft. Azure. Commands. COMPUTE. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="77555-126">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="77555-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="77555-127">NOTES</span></span>

## <span data-ttu-id="77555-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77555-128">RELATED LINKS</span></span>

